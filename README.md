# Amazon Polly Text-to-Speech Project

## What is Amazon Polly?

Amazon Polly is a service provided by AWS that enables developers to generate human-like speech from text.

- **Text-to-Speech Conversion:** Amazon Polly turns written text into spoken words, providing natural-sounding speech.
- **Realistic Speech:** The generated speech sounds like a real person, enhancing user experience.
- **Customization Options:** Users can customize speech speed, pitch, accents, languages, and more.
- **Multilingual and Diverse Voices:** Amazon Polly supports multiple languages and offers a variety of voices, including different accents and genders.
- **SSML Support:** Special codes like SSML allow fine-tuning of speech attributes, such as emphasis, pauses, and tone.

## Getting Started with Amazon Polly

1. **Try Amazon Polly:**
   - Login to your AWS management console.
   - Search for Amazon Polly in the search bar.

2. **Engines and Languages:**
   - Amazon Polly provides different engines and languages for varied speech requirements.

3. **Customization:**
   - Choose language, voice tone, and other parameters for tailored speech output.

4. **Generate Audio:**
   - Input text to be translated into audio.
   - Listen to the output or download/save it.

## Setting Up AWS Resources

### 1. Creating an IAM Role
   - Navigate to IAM in the AWS console.
   - Create a new role with appropriate permissions:
     - AmazonPollyFullAccess
     - AmazonS3FullAccess
     - AWSLambdaBasicExecutionRole

### 2. Creating an S3 Bucket
   - Navigate to S3 in the AWS console.
   - Create a new bucket for storing audio files.

### 3. Creating a Lambda Function
   - Navigate to Lambda in the AWS console.
   - Create a new Lambda function with Node.js 16.x runtime.
   - Use the existing IAM role created earlier.
   - Configure the Lambda function to interact with Amazon Polly and S3.

## Note on Lambda Function Code

The Lambda function code required for this project is provided in the repository. The code is named `index.js` and is written in Node.js 16.x runtime environment.

To use the Lambda function code effectively:

1. **Customize the Voice:** Inside the Lambda function code, you can customize the voice by changing the `VoiceId` parameter. For example, you can replace `'Joanna'` with another voice ID available in Amazon Polly.

2. **Configure S3 Bucket:** Update the S3 bucket name in the Lambda function code. Replace `'your-bucket-name'` with the actual name of your S3 bucket where you want to store the audio files.

3. **Testing and Deployment:** After customizing the code, test the Lambda function using test events in the AWS Lambda console. Ensure that the IAM role attached to the Lambda function has necessary permissions to interact with Amazon Polly and S3.

By following these steps, you can effectively deploy and use the Lambda function for text-to-speech conversion using Amazon Polly.

###Architecture Image

![Architectural Diagram](https://github.com/bhaveshjadhav/text-narrator-using-Amazon-Polly/assets/78265026/18e20fed-5bb0-45aa-94d6-f77d44e2ba1d)
