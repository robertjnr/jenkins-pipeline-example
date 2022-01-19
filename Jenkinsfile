    //Here we created data through json object that we can send along with POST request
    JSONObject requestParams = new JSONObject();
    requestParams.put("name", "abc");
    requestParams.put("age", "10");
    requestParams.put("salary", "10000");

    // specifying headers here, stating that the request body is json
    httpRequest.header("Content-Type", "application/json");

    // add the json body to the request payload
    httpRequest.body(requestParams.toJSONString());

    // Sending POST request
    Response response = httpRequest.request(Method.POST, "/api/v1/create");

    //capturing response body to perform validations
    String responseBody = response.getBody().asString();
    Reporter.log(responseBody); // to log the response

    // to capture response code through getStatusCode method.
    int status = response.getStatusCode();

    Assert.assertEquals(status, 200);
}
