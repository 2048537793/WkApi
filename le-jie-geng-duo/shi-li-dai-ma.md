# 示例代码

### Java  Demo（已废弃，建议直接查看postman示例）

```text
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\n    \"account\": \"18012234567\",\n    \"password\": \"theerea\"\n}");
Request request = new Request.Builder()
  .url("http://xingshenwk.com/member/login")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();




OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\n    \"wcId\":\"wxid_wl9qchkanp9u22\",\n    \"type\": 2\n}");
Request request = new Request.Builder()
  .url("http://xingshenwk.com//iPadLogin")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .addHeader("Authorization", "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJwYXNzd29yZCI6ImUxMGFkYzxxxxxxxxxxx")
  .build();
Response response = client.newCall(request).execute();



OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\n\t\"wId\": \"00000170-84b3-2f54-0010-dac47xxxxxx\"\n}");
Request request = new Request.Builder()
  .url("http://xingshenwk.com//getIPadLoginInfo")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .addHeader("Authorization", "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJwYXNzd29yZCI6ImUxMGFkYzxxxxxxxxxxx")
  .build();
Response response = client.newCall(request).execute();
```

