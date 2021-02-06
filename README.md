# COMP4102-Project
## TA Grading Assistant
#### Members: Matthew Kaprielian-Seferian

### Summary
The plan for this assignment will be to create an assistant for TA’s that will OCR scan the handwritten names and student numbers from student quizzes. It will be using a database of student names and ID’s from the class and will match the written information to the information in the database. This will allow easy organization of tests as well as allowing the TA’s to easily see if they are missing any tests and by which student.

### Background
This project will require users to have access to a camera most likely to be a phone. The user will take a picture of the handwritten name and student number in one image. It will than feed all of them into the program.

### The Challenge
This problem is challenging for a few reasons, first I will have to implement OCR capabilities with OpenCV using Tesseract as OpenCV does not do this natively. Once I have extracted the handwritten data I will have to find and extract the students name and number from the text I have pulled and make sure that it matches with one in the class database. While this may be easy in some contexts depending on the type of test being taken and the picture the program is given it can also prove quite difficult as a math test will have other numbers on the page as well as potentially other names given in questions. I have been interested in OCR capabilities for a while now and being able to work on a project using it that may serve to help other people in the future is wonderful. Using Tesseract to OCR tests while also identifying and extracting the information that I need from the OCR scan will be a great foot in the door to the world of OCR and OpenCV.

### Goals and Deliverables
For this project to be considered a success it will need to first be fed a database for the class including the name and student number of all registered students, it will than receive images of the test papers with student names and numbers on them and OCR these. Once the image is OCR’d it will extract the student name and number, making sure it matches up with one from the database, and display the information. Once the user has finished scanning in all of the assignments the program will let the user know which students if any were not recorded or if any could not be matched at all, then bringing up the images of the ones that could not be matched. Given extra time on the project I would include a functionality for the images to all be renamed with their respective student names and numbers and put into a separate folder along with a text document that shows all of the results. If I somehow finish super early, I will add the functionality to submit two pictures at a time one with a name and one with a number and the program will match them together, this may come up if a student writes their name and number on separate pages.

To test that my project works I will print out 10 copies of a fake test and I will fill in 10 students names and numbers in a mock class (the names will be written by the 4 people that are in my house since with COVID-19 I can’t easily grab 10 people, this is for the greatest diversity in hand writing). I will also include an 11th test that includes a name and number that is not registered in the course and the database that is fed to the program will include a student whose test was not submitted. This will demonstrate the full scope of the program.

### Schedule
February 6th – February 12th: I will spend this week familiarizing myself with both OpenCV as it is a program, I have never used along with Python which I have not used in 3 years (It has been the same length of time for C++ and I prefer to use Python).

February 13th – February 19th: The first step of this project will be to use OpenCV’s text detector to recognize all the text in the image. This uses only built in OpenCV functions and will give us X and Y coordinates of the text.

February 20th – February 26th: Now that the text detection is done, I will extract the detected text and send it to Tesseract which will be performing the OCR on the detected text.

February 27th – March 5th: This week I will build the part of the program that will create the database. This database will be in the form of an excel document with a column for student names and a column for student numbers.

March 6th – March 12th: This week I will match up the names retrieved via OCR to names that are stored in the database and mark names that have been found.

March 13th – March 19th: I will work out the edge cases such as duplicate students, a student name that isn’t in the class database, missing students, and names and numbers that could not be matched at all.

March 20th – March 26th: This week I will make the output file which is easily readable. This will consist of all students that were matched as well as all who weren’t and any issues that the program found.

March 27th – April 2nd: I will now take the time to improve on the database that is imported. I will allow for different file types such as a txt file and a csv file, and I will also allow the program to search for the columns of student names and numbers since I assume any file with this information pulled from the school will come with extra information that we do not need.


April 3rd – April 9th: This week will be reserved for ironing out all bug in the program as well as a buffer in the case that I exceed my current time estimates.

April 10th – April 14th: The program will be ready to present in to the class
