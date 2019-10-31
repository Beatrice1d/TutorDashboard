https://jobs.crossover.com/application


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <title>
        Tutor Dashboard
    </title>
    <meta content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0, shrink-to-fit=no' name='viewport' />
    <!--     Fonts and icons     -->
    <link href="https://fonts.googleapis.com/css?family=Montserrat:400,700,200" rel="stylesheet" />
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/latest/css/font-awesome.min.css" rel="stylesheet">
    <!-- CSS Files -->
    <link href="css/bootstrap.min.css" rel="stylesheet" />
    <link href="css/paper-dashboard.css" rel="stylesheet" />
</head>

<body class="">
    <div class="wrapper ">
        <div class="sidebar" data-color="white" data-active-color="danger">

            <div class="logo">
                <a href="http://startng.ml">

                    <img class="img-fluid w-50 mt-3 mb-1" src="https://res.cloudinary.com/sgnolebagabriel/image/upload/v1570873250/startng/Logo_1_ib5bjh.png">

                </a>

            </div>
            <div class="sidebar-wrapper">
                <ul class="nav">
                    <li class="active">
                        <a href="dashboard.html">
                            <i class="fa fa-home"></i>
                            <p>Dashboard</p>
                        </a>
                    </li>
                    <li>
                        <a href="tutor-profile.html">
                            <i class="fa fa-user"></i>
                            <p>Tutor Profile</p>
                        </a>
                    </li>
                    <li>
                        <a href="view-student.html">
                            <i class="fa fa-users"></i>
                            <p>View Students</p>
                        </a>
                    </li>
                    <li>
                        <a href="upload-resource.html">
                            <i class="fa fa-file"></i>
                            <p>Upload Resource</p>
                        </a>
                    </li>
                    <li>
                        <a href="assignment.html">
                            <i class="fa fa-file"></i>
                            <p>Create Assignments</p>
                        </a>
                        </li>
                </ul>
            </div>
        </div>
        <div class="main-panel">
            <!-- Navbar -->
           36 <nav class="navbar navbar-expand-lg navbar-absolute fixed-top navbar-transparent">
                <div class="container-fluid">
                    <div class="navbar-wrapper">
                        <div class="navbar-toggle">
                            <button type="button" class="navbar-toggler">
                                <span class="navbar-toggler-bar bar1"></span>
                                <span class="navbar-toggler-bar bar2"></span>
                                <span class="navbar-toggler-bar bar3"></span>
                            </button>
                        </div>
                        <a class="navbar-brand" href="#pablo">DASHBOARD</a>
                    </div>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navigation" aria-controls="navigation-index" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-bar navbar-kebab"></span>
                        <span class="navbar-toggler-bar navbar-kebab"></span>
                        <span class="navbar-toggler-bar navbar-kebab"></span>
                    </button>
                    <div class="collapse navbar-collapse justify-content-end" id="navigation">
                        <form>
                            <div class="input-group no-border">
                                <input type="text" value="" class="form-control" placeholder="Search...">
                                <div class="input-group-append">
                                    <div class="input-group-text">
                                        <i class="fa fa-search"></i>
                                    </div>
                                </div>
                            </div>
                        </form>

                    </div>
                </div>
            </nav>
            <!-- End Navbar -->
            <!-- <div class="panel-header panel-header-lg">

  <canvas id="bigDashboardChart"></canvas>


</div> -->

<!-- main body -->
<div class="content">
    <div class="row">
      <div class="col-md-12">
        <div class="form-group">
 <div class="container" id="new">
                        
    <form id="review-form" action="#">

            <div class="row">
                    <div class="col-md-12">
                        <div class="form-group">
                            <label for="desc">Question Number</label>
                            <input id="desc" class="form-control" type="text" name="">
                        </div>
                    </div> 
            </div>
            <div class="row">
                    <div class="col-md-12">
                        <div class="form-group">
                            <label for="desc">Question</label>
                            <input id="desc" class="form-control" type="text" name="" placeholder="Type Assignment Question">
                            </div>
                    </div> 
            </div>
                <div class="col-md-12 text-center">
                    <a class="btn btn-warning" href="">SUBMIT</a>
                </div>
    </form>

        <div class="divHolder">
            <h4 class="nameHolder">Question 1</h4>
            <p class="parHolder">Describe the importance of defining variables in JavaScript?</p>
        </div>
        <div class="dynamic"></div>
        </div>
       </div>
    </div> 
</div>



<script>

class Review {
//HERE   ====== ***HERE***
constructor(name, title, msg) {
this.name = name;
this.msg = msg;

//HERE (Complete line)
this.title = title;
}
}

class UI {
addReviewToList(review) {
const list = document.querySelector('.dynamic');

const div = document.createElement('div');
const h4 = document.createElement('h4');
const par = document.createElement('p');
const btn = document.createElement('button');
const btndiv = document.createElement('div');

//HERE (Complete line)
const titlediv = document.createElement('h6');


h4.textContent = `${review.name}`;  
par.textContent = `${review.msg}`;
btn.textContent = 'Delete';

//HERE (Complete line)
titlediv.textContent = `${review.title}`;

div.classList.add("divHolder");
h4.classList.add("nameHolder");
par.classList.add("parHolder");
btn.classList.add("delete");
btndiv.classList.add("test");

//HERE (Complete line)
titlediv.classList.add('new-title');

btndiv.appendChild(btn)
div.appendChild(h4);

//HERE (Complete line)
div.appendChild(titlediv);
div.appendChild(par)
div.appendChild(btndiv)
list.appendChild(div)
}

showAlert(message, className) {
const div = document.createElement('div');
div.className = `alert ${className}`;
div.appendChild(document.createTextNode(message));
const container = document.querySelector('.container');
const form = document.querySelector('#review-form');
container.insertBefore(div, form);

setTimeout(function(){
document.querySelector('.alert').remove();
}, 3000);
}

deleteReview(target) {
if(target.className === 'delete') {
target.parentElement.parentElement.remove();
}
}

clearFields() {
document.getElementById('name').value = '';
document.getElementById('msg').value = '';

//HERE (Complete line)
document.getElementById('title').value = '';
}
}

class Store {
static getReviews() {
let reviews;
if(localStorage.getItem('reviews') === null) {
reviews = [];
} else {
reviews = JSON.parse(localStorage.getItem('reviews'));
}

return reviews;
}

static displayReviews() {
const reviews = Store.getReviews();

reviews.forEach(function(review){
const ui  = new UI;

ui.addReviewToList(review);
});
}

static addReview(review) {
const reviews = Store.getReviews();

reviews.push(review);

localStorage.setItem('reviews', JSON.stringify(reviews));
}

static removeReview(msg) {
const reviews = Store.getReviews();

reviews.forEach(function(review, index){
reviews.splice(index, 1);

});

localStorage.setItem('reviews', JSON.stringify(reviews));
}
}

document.addEventListener('DOMContentLoaded', Store.displayReviews);

document.querySelector('.btn btn-warning').addEventListener('click', function(e){
const name = document.getElementById('name').value;
const msg = document.getElementById('msg').value;

//HERE (Complete line)
const title = document.getElementById('title').value;

//HERE    ================  ** HERE **
let review = new Review(name, title, msg);  
const ui = new UI();

//HERE      =============   *** HERE ***
if(name === '' || msg === '' || title === '') {
ui.showAlert('Please fill in all fields', 'error');
} else {
ui.addReviewToList(review);
Store.addReview(review);
ui.showAlert('Comment Submitted!', 'success');
ui.clearFields();
}

e.preventDefault();
});
                    // ****Double click edit HERE**** (Change from 'click' to 'dbclick')
document.querySelector('.dynamic').addEventListener('dblclick' , function(e){  
const ui = new UI();
ui.deleteReview(e.target);
Store.removeReview(e.target.parentElement.parentElement.textContent);
ui.showAlert('Comment Deleted!', 'success');

e.preventDefault();
});

</script>

</body>
</html>



































# TutorDashboard


https://cramwordplay.github.io/StartNg-2/tutor-dashboard.html

https://docs.google.com/forms/u/2/d/e/1FAIpQLSe_jMpA9lbiGE1Vcyn70TkS0hCGZKOnXXz8Z4YN2C9-Sh4Lwg/viewform?usp=pp_url

https://www.pivotaltracker.com/n/projects/2410002/stories/169433709



https://docs.google.com/forms/d/e/1FAIpQLScZLOQ89sXLDAFZBGgrMK_eGrXospAoFVhUSO_IHi1YL9vT7Q/viewform?usp=pp_url
