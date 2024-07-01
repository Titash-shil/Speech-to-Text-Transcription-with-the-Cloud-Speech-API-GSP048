# Speech to Text Transcription with the Cloud Speech API || [GSP048](https://www.cloudskillsboost.google/course_templates/756/labs/475241) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

* ### Run the following Commands in Cloudshell
```
gcloud services enable apikeys.googleapis.com
gcloud alpha services api-keys create --display-name="techcps"
CP=$(gcloud alpha services api-keys list --format="value(name)" --filter "displayName=techcps")
API_KEY=$(gcloud alpha services api-keys get-key-string $CP --format="value(keyString)")

cat > request.json <<EOF_CP
{
  "config": {
      "encoding":"FLAC",
      "languageCode": "en-US"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/brooklyn_bridge.flac"
  }
}
EOF_CP

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json
cat result.json
```
##  Check your progress on Task 1-3 
##  Do not run the next command until you get the score on Task 1-3
```
cat > request.json <<EOF_CP
 {
  "config": {
      "encoding":"FLAC",
      "languageCode": "fr"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/corbeau_renard.flac"
  }
}
EOF_CP

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json
cat result.json
```

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
