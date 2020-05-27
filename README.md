/User should be able to register./

package com.journaldev.utils; import java.io.BufferedReader; import java.io.IOException; import java.io.InputStreamReader; import java.io.OutputStream; import java.net.HttpURLConnection; import java.net.URL;

public class ArticleExample {

private static final String USER_AGENT = "Mozilla/5.0";

private static final String GET_URL = "https://localhost:9090/SpringMVCExample";

private static final String POST_URL = "https://localhost:9090/SpringMVCExample/home";

private static final String POST_PARAMS = "userName=abinash";

private static final String POST_PARAMS1 = "password=simpragma123";

public static void main(String[] args) throws IOException {
	sendGET();
	System.out.println("GET DONE");
	sendPOST();
	System.out.println("POST DONE");
}

private static void sendGET() throws IOException {
	URL obj = new URL(GET_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("GET");
	con.setRequestProperty("User-Agent", USER_AGENT);
	int responseCode = con.getResponseCode();
	System.out.println("GET Response Code :: " + responseCode);
	if (responseCode == HttpURLConnection.HTTP_OK) { // success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("GET request not worked");
	}
    }
private static void sendPOST() throws IOException {
	URL obj = new URL(POST_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("POST");
	con.setRequestProperty("User-Agent", USER_AGENT);
	// For POST only - START
	con.setDoOutput(true);
	OutputStream os = con.getOutputStream();
	os.write(POST_PARAMS.getBytes());
	os.flush();
	os.close();
	// For POST only - END

	int responseCode = con.getResponseCode();
	System.out.println("status Code":"201");
			System.out.println("new article created");

	if (responseCode == HttpURLConnection.HTTP_OK) { //success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("POST request not worked");
	}
    }
    }
	/***User should be able to login.***/
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "https://www.w3.org/TR/html4/loose.dtd">
<title>Create Article Page</title>



/User should be able to add an article./

<title>List Article</title>



/User should be able to view all articles./

package com.journaldev.utils; import java.io.BufferedReader; import java.io.IOException; import java.io.InputStreamReader; import java.io.OutputStream; import java.net.HttpURLConnection; import java.net.URL;

public class List Article Example {

private static final String USER_AGENT = "Mozilla/5.0";

private static final String GET_URL = "https://localhost:9090/SpringMVCExample";

private static final String POST_URL = "https://localhost:9090/SpringMVCExample/home";

private static final String POST_PARAMS = "userName=abinash";

private static final String POST_PARAMS1 = "password=simpragma123";

public static void main(String[] args) throws IOException {
	sendGET();
	System.out.println("GET DONE");
	sendPOST();
	System.out.println("POST DONE");
}

private static void sendGET() throws IOException {
	URL obj = new URL(GET_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("GET");
	con.setRequestProperty("User-Agent", USER_AGENT);
	int responseCode = con.getResponseCode();
	System.out.println("GET Response Code :: " + responseCode);
	if (responseCode == HttpURLConnection.HTTP_OK) { // success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("GET request not worked");
	}
    }
private static void sendPOST() throws IOException {
	URL obj = new URL(POST_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("POST");
	con.setRequestProperty("User-Agent", USER_AGENT);
	// For POST only - START
	con.setDoOutput(true);
	OutputStream os = con.getOutputStream();
	os.write(POST_PARAMS.getBytes());
	os.flush();
	os.close();
	// For POST only - END
	int responseCode = con.getResponseCode();
	System.out.println("status Code":"200");
			System.out.println("new article created");

	if (responseCode == HttpURLConnection.HTTP_OK) { //success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("POST request not worked");
	}
    }
    }
/Article listing should be paginated./

<title>Login Page</title>
package com.journaldev.utils; import java.io.BufferedReader; import java.io.IOException; import java.io.InputStreamReader; import java.io.OutputStream; import java.net.HttpURLConnection; import java.net.URL;

public class LoginExample {

private static final String USER_AGENT = "Mozilla/5.0";

private static final String GET_URL = "https://localhost:9090/SpringMVCExample";

private static final String POST_URL = "https://localhost:9090/SpringMVCExample/home";

private static final String POST_PARAMS = "userName=abinash";

private static final String POST_PARAMS1 = "password=simpragma123";

public static void main(String[] args) throws IOException {
	sendGET();
	System.out.println("GET DONE");
	sendPOST();
	System.out.println("POST DONE");
}

private static void sendGET() throws IOException {
	URL obj = new URL(GET_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("GET");
	con.setRequestProperty("User-Agent", USER_AGENT);
	int responseCode = con.getResponseCode();
	System.out.println("GET Response Code :: " + responseCode);
	if (responseCode == HttpURLConnection.HTTP_OK) { // success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("GET request not worked");
	}
    }
private static void sendPOST() throws IOException {
	URL obj = new URL(POST_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("POST");
	con.setRequestProperty("User-Agent", USER_AGENT);
	// For POST only - START
	con.setDoOutput(true);
	OutputStream os = con.getOutputStream();
	os.write(POST_PARAMS.getBytes());
	os.flush();
	os.close();
	// For POST only - END

	int responseCode = con.getResponseCode();
	System.out.println("status Code":"200");
	if (responseCode == HttpURLConnection.HTTP_OK) { //success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("POST request not worked");
	}
    }
    }

	<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "https://www.w3.org/TR/html4/loose.dtd">
<title>Register Page</title>



package com.journaldev.utils; import java.io.BufferedReader; import java.io.IOException; import java.io.InputStreamReader; import java.io.OutputStream; import java.net.HttpURLConnection; import java.net.URL;

public class RegisterExample {

private static final String USER_AGENT = "Mozilla/5.0";

private static final String GET_URL = "https://localhost:9090/SpringMVCExample";

private static final String POST_URL = "https://localhost:9090/SpringMVCExample/home";

private static final String POST_PARAMS = "userName=abinash";

private static final String POST_PARAMS1 = "password=simpragma123";

private static final String POST_PARAMS1 = "email=abinash@simpragma.com";
	
private static final String POST_PARAMS1 = "address=bangalore";



public static void main(String[] args) throws IOException {
	sendGET();
	System.out.println("GET DONE");
	sendPOST();
	System.out.println("POST DONE");
}

private static void sendGET() throws IOException {
	URL obj = new URL(GET_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("GET");
	con.setRequestProperty("User-Agent", USER_AGENT);
	int responseCode = con.getResponseCode();
	System.out.println("GET Response Code :: " + responseCode);
	if (responseCode == HttpURLConnection.HTTP_OK) { // success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("GET request not worked");
	}
    }
private static void sendPOST() throws IOException {
	URL obj = new URL(POST_URL);
	HttpURLConnection con = (HttpURLConnection) obj.openConnection();
	con.setRequestMethod("POST");
	con.setRequestProperty("User-Agent", USER_AGENT);
	// For POST only - START
	con.setDoOutput(true);
	OutputStream os = con.getOutputStream();
	os.write(POST_PARAMS.getBytes());
	os.flush();
	os.close();
	// For POST only - END

	int responseCode = con.getResponseCode();
	System.out.println("status Code":"201");
	System.out.println("new user created");

	if (responseCode == HttpURLConnection.HTTP_OK) { //success
		BufferedReader in = new BufferedReader(new InputStreamReader(
				con.getInputStream()));
		String inputLine;
		StringBuffer response = new StringBuffer();

		while ((inputLine = in.readLine()) != null) {
			response.append(inputLine);
		}
		in.close();

		// print result
		System.out.println(response.toString());
	} else {
		System.out.println("POST request not worked");
	}
    }
    }
