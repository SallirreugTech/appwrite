import 'package:dart_appwrite/dart_appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>') // Your project ID
    .setKey('<YOUR_API_KEY>'); // Your secret API key

Users users = Users(client);

User result = await users.createSHAUser(
    userId: '<USER_ID>',
    email: 'email@example.com',
    password: 'password',
    passwordVersion: PasswordHash.sha1, // (optional)
    name: '<NAME>', // (optional)
);