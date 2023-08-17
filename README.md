
## My deployment Documentation
<h1>Deploying a URL Shortener application</h1>


<ol style="text-align:center;">
<li>Downloaded the files from Kura and uploaded to a new repository which I named Deploy01</li>
<li>Signed into the instructor's Jenkin's server</li>
<li>Built the Jenkins pipeline</li>
<h2><em>When running the jenkins pipeline I ran into some issues:</em> </h2>
 <p>All the stages failed reason being the jenkins server could not find the jenkins file.Upon further analysis it was noted that my files and folders in Deploy01 repository were in a c4 folder and the jenkins server expected the files to be in the /main path specified.I removed all the files and folders from the c4 folder in that way they were all in /main. This fixed all issues and the pipe line ran as expected</p>
<li>The next step was to zip the files and folder</li>
<li>Next it was time to head to AWS and Created My EC2 and AWS ElasticBeanstalk</li> 
<li>I proceeded through all the steps as given, when it was time to run the ElasticBeanStalk the healthy status returned "Degraded" and the link responded with a "502 Bad Gateway nginx"</li>
  
<h2><em>What could be the possible reason for this response?</em></h2>
<ul>
<li> I did not zip the files properly</li>
-> I fixed this issue by unzipping the downloaded zip file I got from repository,opening the unzipped folder and highlighting over all files inside and zipping up those again<br><br>
-> I deleted the old ElasticBeanStalk and configured a new one following all the steps, this time using the properly zipped files and the health status responded with a green Healthy response signifying everything was successful<br><br>
-> I tested the link out and it returned a front end of a url shortener application: <br><br>
  
  <img width="1432" alt="Screenshot 2023-08-17 at 3 19 31 PM" src="https://github.com/NMonKLabs77/Deploy01/assets/139259756/40484485-3635-4bef-abbf-6e516d418649">
</ul>  
</ol>
<h2>My Plan</h2>

  <img width="932" alt="Screenshot 2023-08-16 at 3 46 40 PM" src="https://github.com/NMonKLabs77/Deploy01/assets/139259756/732e90fb-e8da-4385-b8fc-9f0c24eb5bf4">



  
