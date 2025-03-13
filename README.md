<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Abderrahmane - Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <!-- Header Section -->
    <header>
      <h1>
        <span class="greeting">Hi, my name is</span>
        <span class="name">Abderrahmane</span>
      </h1>
      <p>I'm a computer science engineering student</p>
    </header>

    <!-- Profile Photo -->
    <div class="profile-photo">
      <img src="https://assets.onecompiler.app/434b9smgd/43bmem6dj/Picsart_25-01-08_12-01-09-311.jpg" alt="Abderrahmane">
    </div>

    <!-- Skills Section -->
    <div class="skills">
      <h2 class="skills-title">My Skills</h2>
      <div class="skill-icons">
        <img src="https://assets.onecompiler.app/434b9smgd/43bmem6dj/pngwing.com%20(3).png" alt="HTML" class="skill-icon">
        <img src="https://assets.onecompiler.app/434b9smgd/43bmem6dj/pngwing.com%20(5).png" alt="CSS" class="skill-icon">
        <img src="https://assets.onecompiler.app/434b9smgd/43bmem6dj/pngwing.com%20(6).png" alt="JavaScript" class="skill-icon">
      </div>
    </div>

    <!-- Contact Section -->
    <div class="contact">
      <h2>Contact Me</h2>
      <p>Email: <a href="mailto:abdoudha4@gmail.com">abdoudha4@gmail.com</a></p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
/* General Styles */
body {
  margin: 0;
  padding: 0;
  font-family: 'Arial', sans-serif;
  background: linear-gradient(135deg, #0a192f, #1a365f);
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  overflow-x: hidden;
}

.container {
  text-align: center;
  width: 90%;
  max-width: 800px;
  padding: 20px;
  margin: 20px 0;
}

/* Header Section */
header h1 {
  font-size: 2rem;
  margin-bottom: 10px;
}

header p {
  font-size: 1rem;
  color: #64ffda;
}

/* Greeting + Name Decoration */
.greeting,
.name {
  background: linear-gradient(45deg, #64ffda, #00bcd4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: bold;
  display: inline-block;
  animation: float 6s ease-in-out infinite;
  position: relative;
}

.greeting::after,
.name::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 3px;
  background: linear-gradient(45deg, #64ffda, #00bcd4);
  bottom: -5px;
  left: 0;
  transform: scaleX(0);
  transition: transform 0.5s ease;
}

.greeting:hover::after,
.name:hover::after {
  transform: scaleX(1);
}

/* Profile Photo */
.profile-photo {
  margin: 30px 0;
}

.profile-photo img {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  border: 4px solid #64ffda;
  animation: float 6s ease-in-out infinite;
}

/* Skills Section */
.skills {
  margin-top: 50px;
}

.skills-title {
  font-size: 1.5rem;
  background: linear-gradient(45deg, #64ffda, #00bcd4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: bold;
  animation: float 6s ease-in-out infinite;
  position: relative;
  display: inline-block;
}

.skills-title::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 3px;
  background: linear-gradient(45deg, #64ffda, #00bcd4);
  bottom: -5px;
  left: 0;
  transform: scaleX(0);
  transition: transform 0.5s ease;
}

.skills-title:hover::after {
  transform: scaleX(1);
}

.skill-icons {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
  margin-top: 20px;
}

.skill-icon {
  width: 50px;
  height: 50px;
  animation: float 4s ease-in-out infinite;
}

.skill-icon:nth-child(2) {
  animation-delay: 1s;
}

.skill-icon:nth-child(3) {
  animation-delay: 2s;
}

/* Contact Section */
.contact {
  margin-top: 50px;
}

.contact h2 {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.contact a {
  color: #64ffda;
  text-decoration: none;
}

.contact a:hover {
  text-decoration: underline;
}

/* Floating Animation */
@keyframes float {
  0%, 100% {
    transform: translateY(0);
    text-shadow: 0 0 10px rgba(100, 255, 218, 0.5);
  }
  50% {
    transform: translateY(-20px);
    text-shadow: 0 0 20px rgba(100, 255, 218, 0.8);
  }
}

/* Responsive Design */
@media (min-width: 768px) {
  header h1 {
    font-size: 2.5rem;
  }

  header p {
    font-size: 1.2rem;
  }

  .profile-photo img {
    width: 150px;
    height: 150px;
  }

  .skills-title {
    font-size: 1.8rem;
  }

  .contact h2 {
    font-size: 1.8rem;
  }
}
