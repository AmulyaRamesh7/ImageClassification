 git clone https://github.com/AmulyaRamesh7/ImageClassification.git
  cd ImageClassification
 echo "original content">file.txt
$ git add .
$ git commit -m "initail commite"
$ git checkout -b feature
$ echo "feature added">file.txt
$ git add .
$ git commit -m "added feature"
$ git checkout main
$ echo "main branch content">file.txt
$ git add .
$ git commit -m "main change"
$ git merge feature
$ pwd
/c/Users/Amulya Ramesh/ImageClassification
$ git add file.txt
$ git commit -m "resolved merge conflict"
$ git checkout feature
$ git rebase main
  9th
  <!DOCTYPE html>
<html>
    <head>
        <title> Task Manager </title>
        <!-- jQuery CDN -->
         <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    </head>
    <body>
        <h2> Task Manager </h2>
        <input type="text" id="taskInput" placeholder="Enter a task">
        <button id="addTask">Add Task</button>

        <h3>Tasks:</h3>
        <ul id="tasklist"></ul>


        <script src="script.js"></script>
    </body>
</html>

5. create script.js

$(document).ready(function(){
    // Addtask
    $("#addTask").click(function(){
        let task = $("#taskInput").val();
        if(task){
            $("#tasklist").append("<li>" + task + " <button class='remove'>Remove</button></li>");
            $("#taskInput").val("");
        }
    });

    // Remove task
    $(document).on("click", ".remove", function(){
        $(this).parent().remove();
    });

    // Retrieve all tasks
    function getTasks(){
        let tasks = [];
        $("#tasklist li").each(function(){
            tasks.push($(this).text().replace(" Remove", ""));
        });
        return tasks;
    }

    // Log tasks whenever list changes
    $("#tasklist").on("DOMSubtreeModified", function(){
        console.log("current Tasks:", getTasks());
    });
});
8th 
Create folder in desktop (DockerDemo)
Open vs code select folder DockerDemo

Create file (index.html)

<!DOCTYPE html>
<html>
<head>
    <title>Docker Demo</title>
</head>
<body>
    <h1>Hello from Docker!</h1>
    <h2>DevOps Practical</h2>
</body>
</html>

Create another file (Dockerfile)

FROM nginx
COPY index.html /usr/share/nginx/html/index.html

Next open commd promt and do this step

1. docker --version
2. docker info
3. docker pull nginx
4. docker images
5. docker run -d nginx
6. docker ps
7. docker ps -a
8. docker stop (container_id)
9. docker rm  (container _id)
10. docker rmi (image id)
11. cd DockerDemo
12. docker build -t myimage .
13. docker run -d -p 8081:80 myimage
14. Open chrome and type http://localhost:8081
