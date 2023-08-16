
## My deployment Documentation
---Deploying a URL Shortener application--

- Downloaded the files from Kura and uploaded to a new repository which I named Deploy01
- Signed into the instructor's Jenkin's server
- Built the Jenkins pipeline
- When running the jenkins pipeline I ran into some issues:
  1) All the stages failed reason being the jenkins server could not find the jenkins file.Upon further analysis it was noted that my files and folders in Deploy01 repository were in a c4 folder and the jenkins server expected the files to be in the /main path specified.I removed all the files and folders from the c4 folder in that way they were all in /main. This fixed all issues and the pipe line ran as expected.
- The next step was to zip the files and folder.
- Next it was time to head to AWS and Created My EC2 and AWS ElasticBeanstalk
- I proceeded through all the steps as given, when it was time to run the ElasticBeanStalk the healthy status returned "Degraded" and the link responded with a "502 Bad Gateway nginx".
What could be the possible reason for this response?
-It turned out that I did not zip the files properly.
  -I fixed this issue by unzipping the downloaded zip file I got from repository,opening the unzipped folder and highlighting over all files inside and zipping up those again
- I deleted the old ElasticBeanStalk and configured a new one following all the steps, this time using the properly zipped files and the health status responded with a green Healthy response signifying everything was successful.
- I tested the link out and it returned a front end of a url shortener application
- Finally, I uploaded and deployed.

  <img width="932" alt="Screenshot 2023-08-16 at 3 46 40 PM" src="https://github.com/NMonKLabs77/Deploy01/assets/139259756/732e90fb-e8da-4385-b8fc-9f0c24eb5bf4">



  
