import { Client, Teams } from "react-native-appwrite";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

const teams = new Teams(client);

const result = await teams.deleteMembership(
    '<TEAM_ID>', // teamId
    '<MEMBERSHIP_ID>' // membershipId
);

console.log(result);