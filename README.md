# Logstash Dockerfile

This configuration can be used to read data from twitter and push it into an AWS Elastic Service.

# Supported version:

TAG 6.2 : support Elastic 6.2.
Last: see TAG 6.2


# How to use this image

this container need to set environment variables before starting:

##  Twitter configuration

TWITTER_CONSUMER_KEY:
TWITTER_CONSUMER_SECRET:
TWITTER_OAUTH_TOKEN:
TWITTER_OAUTH_SECRET:
TWITTER_KEY_WORDS: Currently limited for one word.

## AWS configuration

AWS_HOST
AWS_REGION
AWS_ACCESS_KEY
AWS_ACCESS_SECRET

**To start a basic container**

docker run  -it -e TWITTER_CONSUMER_KEY='your consumer key' \
-e TWITTER_CONSUMER_SECRET='your consumer secret' \
-e TWITTER_OAUTH_TOKEN='your token' \
-e TWITTER_OAUTH_SECRET='your token secret' \
-e TWITTER_KEY_WORDS='TER_Metz_Lux' \
-e AWS_HOST='aws-host-name' \
-e AWS_REGION='eu-west-3' \
-e AWS_ACCESS_KEY='your iam aws acces key' \
-e AWS_ACCESS_SECRET='your iam aws acces secret' \
--name jocelyn57/logstash-aws-twitter:6.2
