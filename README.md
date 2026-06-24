[Deploying a Python Flask Application Using Docker.docx](https://github.com/user-attachments/files/29293639/Deploying.a.Python.Flask.Application.Using.Docker.docx)
Deploying a Python Flask Application Using Docker


1. Objective
The objective of this assignment is to deploy a Python Flask application using Docker, build a Docker image, run the container locally, and verify the application through a web browser.

2. Repository Used
•	Repository URL: https://github.com/shelgepavan7/flask-app.git

3. Commands Used
Clone Repository
•	https://github.com/shelgepavan7/flask.git

Build Docker Image
•	docker build -t flask-app .
Verify Image
•	docker images

 
 
Run Docker Container
•	docker run -d -p 5000:5000 flask-app
Verify Running Container
•	docker ps
 
4. Dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["python", "app.py"]
 

Commands Used
•	docker –version
•	docker images
•	docker logs flask-app
•	git init
•	git add .
•	git commit -m “flask docker assignment”
•	git remote add origin
•	git push -u origin main
•	docker build -t flask-app .
•	docker run -d -p 5000:5000 flask-app
•	docker ps


5. Verification
•	After running the container, the application was successfully accessed using:
•	http://localhost:5000
 

 
6. Issues Faced and Resolution
Issue 1
•	Docker image build failed because Flask dependency was missing.
Resolution
•	Created requirements.txt and installed dependencies using pip.
Issue 2
•	Application was not accessible from browser.
Resolution
•	app.run(host="0.0.0.0", port=5000)


7. Conclusion
Successfully containerized the Flask application using Docker, built and run the image locally, and verified the application through a web browser. This exercise demonstrated basic Docker containerization and deployment concepts.




