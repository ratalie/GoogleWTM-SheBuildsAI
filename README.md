# GoogleWTM-SheBuildsAI
Google's Women Techmakers presents She Builds AI
# Project Description:
This project aims to inspire and empower young girls by creating personalized motivational videos that are tailored to their dreams and aspirations. Girls from around the world submit their career goals, backgrounds, and personal stories through a multi-modal platform. The platform uses AI to process these submissions (text, video, handwritten), matches them with a role model from a diverse pre-existing database, and generates a personalized, one-minute inspirational video.

The project addresses gender inequality by:

Providing girls in remote or underserved communities access to powerful role models, regardless of geographic barriers.
Encouraging girls to pursue leadership roles and ambitious career paths, inspired by women who have achieved success in those fields.
Offering practical advice and follow-up resources in the videos, helping girls understand the steps they need to take to realize their dreams.
Through this platform, we hope to promote gender equality by giving young girls the motivation and confidence to pursue leadership roles in their chosen fields.

# Setup 
# 1. Environment
Enable Google Gemini (Gemma) for multi-modal data processing.
Enable Google Cloud Storage for file management (video uploads, text, and handwriting).
Enable Google AI API for natural language processing (NLP) and image recognition.
Set up a Google Cloud Function for processing the data: https://github.com/ratalie/GoogleWTM-SheBuildsAI/blob/main/1-dataprocessingGCP
# 2. Collect Data
Google Forms to collect data from girls. The form collects the following information:
- Their dream/aspiration.
- Any background information (text, video, or handwriting).
- Country, age, and language preference.
Integrate the form with Google Sheets to store responses and set up a trigger that runs whenever a new form is submitted.
# 3. Gemma Multimodal
Gemma to process the different types of data (text, video, handwriting). Prepare a pipeline to handle the multi-modal input. https://github.com/ratalie/GoogleWTM-SheBuildsAI/blob/main/3-gemma-multimodal
# 4. Match Girls with Role Models
Use the insights gathered (e.g., career aspirations, key themes) to match each girl with a suitable role model from a pre-existing database. The role model database should contain profiles, including their career path, achievements, and available video clips. https://github.com/ratalie/GoogleWTM-SheBuildsAI/blob/main/4-MatchRolesMwGirls
# 5. Generate the Video
Once the role model is matched, generate the one-minute personalized video by combining pre-recorded role model videos with custom intro/outro text and any specific advice related to the girl’s aspirations.
Google Cloud Video Intelligence API to clips, and personalize it based on the girl's background and goals. https://github.com/ratalie/GoogleWTM-SheBuildsAI/blob/main/5-GenerateVideo
# 6. Make the Video Available
Google Cloud Storage and provide a downloadable link to the girl via a portal. Also, make sure the video can be accessed offline by giving an option for the girl to download it. https://github.com/ratalie/GoogleWTM-SheBuildsAI/blob/main/5-GenerateVideo
# 7. Provide Guidance and Track Progress 
Follow-up plan for each girl, detailing actionable steps to achieve their goals. This can be sent along with the video link, using email or an SMS integration with Google Cloud Messaging.


