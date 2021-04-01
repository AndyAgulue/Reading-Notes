# WRRC and Java (The HTTP Request Lifecycle)[https://www.baeldung.com/java-http-request]

## HTTPUrlConnection

The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package.

The disadvantages of using this method are that the code can be more cumbersome than other HTTP libraries and that it does not provide more advanced functionalities such as dedicated methods for adding headers or authentication.

## Creating a Request

We can create an HttpUrlConnection instance using the openConnection() method of the URL class. Note that this method only creates a connection object but doesn't establish the connection yet.

The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

## Adding Request Parameters

We can create an HttpUrlConnection instance using the openConnection() method of the URL class. Note that this method only creates a connection object but doesn't establish the connection yet.

The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

## Settling Request Headers

We can create an HttpUrlConnection instance using the openConnection() method of the URL class. Note that this method only creates a connection object but doesn't establish the connection yet.

The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

## Configuring Timeouts

HttpUrlConnection class allows setting the connect and read timeouts. These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.

To set the timeout values, we can use the setConnectTimeout() and setReadTimeout() methods:

con.setConnectTimeout(5000);
con.setReadTimeout(5000);

## Handling Cookies

The java.net package contains classes that ease working with cookies such as CookieManager and HttpCookie.

First, to read the cookies from a response, we can retrieve the value of the Set-Cookie header and parse it to a list of HttpCookie objects:

String cookiesHeader = con.getHeaderField("Set-Cookie");
List<HttpCookie> cookies = HttpCookie.parse(cookiesHeader);
Next, we will add the cookies to the cookie store:

cookies.forEach(cookie -> cookieManager.getCookieStore().add(null, cookie));
Let's check if a cookie called username is present, and if not, we will add it to the cookie store with a value of “john”:

Optional<HttpCookie> usernameCookie = cookies.stream()
  .findAny().filter(cookie -> cookie.getName().equals("username"));
if (usernameCookie == null) {
    cookieManager.getCookieStore().add(null, new HttpCookie("username", "john"));

    Finally, to add the cookies to the request, we need to set the Cookie header, after closing and reopening the connection:

con.disconnect();
con = (HttpURLConnection) url.openConnection();

con.setRequestProperty("Cookie", 
  StringUtils.join(cookieManager.getCookieStore().getCookies(), ";"));


## Handling Redirects

We can enable or disable automatically following redirects for a specific connection by using the setInstanceFollowRedirects() method with true or false parameter:

con.setInstanceFollowRedirects(false);
It is also possible to enable or disable automatic redirect for all connections:

HttpUrlConnection.setFollowRedirects(false);
By default, the behavior is enabled.

When a request returns a status code 301 or 302, indicating a redirect, we can retrieve the Location header and create a new request to the new URL:

if (status == HttpURLConnection.HTTP_MOVED_TEMP
  || status == HttpURLConnection.HTTP_MOVED_PERM) {
    String location = con.getHeaderField("Location");
    URL newUrl = new URL(location);
    con = (HttpURLConnection) newUrl.openConnection();
}


## Reading the Responses

Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.

To execute the request, we can use the getResponseCode(), connect(), getInputStream() or getOutputStream() methods:

int status = con.getResponseCode();
Finally, let's read the response of the request and place it in a content String:

BufferedReader in = new BufferedReader(
  new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    content.append(inputLine);
}
in.close();
To close the connection, we can use the disconnect() method:

con.disconnect();


## Reading the Responses on failed Requests

Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.

To execute the request, we can use the getResponseCode(), connect(), getInputStream() or getOutputStream() methods:

int status = con.getResponseCode();
Finally, let's read the response of the request and place it in a content String:

BufferedReader in = new BufferedReader(
  new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    content.append(inputLine);
}
in.close();
To close the connection, we can use the disconnect() method:

con.disconnect();


## Building the Full Response

It's not possible to get the full response representation using the HttpUrlConnection instance.

However, we can build it using some of the methods that the HttpUrlConnection instance offers:

public class FullResponseBuilder {
    public static String getFullResponse(HttpURLConnection con) throws IOException {
        StringBuilder fullResponseBuilder = new StringBuilder();

        // read status and message

        // read headers

        // read response content

        return fullResponseBuilder.toString();
    }
}
Here, we're reading the parts of the responses, including the status code, status message and headers, and adding these to a StringBuilder instance.

First, let's add the response status information:

fullResponseBuilder.append(con.getResponseCode())
  .append(" ")
  .append(con.getResponseMessage())
  .append("\n");
Next, we'll get the headers using getHeaderFields() and add each of them to our StringBuilder in the format HeaderName: HeaderValues:

con.getHeaderFields().entrySet().stream()
  .filter(entry -> entry.getKey() != null)
  .forEach(entry -> {
      fullResponseBuilder.append(entry.getKey()).append(": ");
      List headerValues = entry.getValue();
      Iterator it = headerValues.iterator();
      if (it.hasNext()) {
          fullResponseBuilder.append(it.next());
          while (it.hasNext()) {
              fullResponseBuilder.append(", ").append(it.next());
          }
      }
      fullResponseBuilder.append("\n");
});


