- 👋 Hi, I’m @hasan19377
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
hasan19377/hasan19377 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


<!DOCTYPE html>
<!-- Coding by CodingLab |www.youtube.com/CodingLabYT-->
<html lang="en" dir="ltr">
  <head>
    <meta charset="UTF-8">
    <title> Button with Progress Bar | CodingLab </title>
    <link rel="stylesheet" href="style.css">
    <!-- Boxiocns CDN Link -->
    <link href='https://unpkg.com/boxicons@2.0.7/css/boxicons.min.css' rel='stylesheet'>
   </head>
<body>
  <div class="button ">
    <div class="text-icon">
      <i class="bx bx-cloud-upload"></i>
      <span class="text">Upload File</span>
    </div>
  </div>

  <script>
    const button = document.querySelector(".button"),
    text = document.querySelector(".text");

    button.addEventListener("click", ()=>{
      button.classList.add("progress");
      text.innerText = "Uploading...";

      setTimeout(()=>{
       button.classList.remove("progress"); //remove progress after 6s
       text.innerText = "Uploaded";
      },6000); //1000ms = 1s (6000 = 6s)

    });
  </script>


<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins',sans-serif;
}
body{
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #F4F7FF;
}
.button{
  position: relative;
  height: 200px;
  max-width: 200px;
  width: 100%;
  background: linear-gradient(#7B0A0A,#002FFF);
  border-radius: 50%;
  cursor: pointer;
  box-shadow: 0 5px 10px rgba(0,0,0,0.2);
  overflow: hidden;
}
.button::before{
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  height: 100%;
  width: 100%;
  background: rgba(0,0,7,0.2);
  border-radius: 6px;
}
.button.progress::before{
  animation: progress 6s ease-in-out forwards;
}
@keyframes progress {
  0%{
    left: -100%;
  }
  10%{
    left: -97%;
  }
  20%{
    left: -92%;
  }
  30%{
    left: -82%;
  }
  30%{
    left: -62%;
  }
  40%{
    left: -38%;
  }
  50%{
    left: -18%;
  }
  60%{
    left: -14%;
  }
  80%{
    left: -7%;
  }
  90%{
    left: -3%;
  }
  100%{
    left: 0%;
  }
}
.button .text-icon{
  height: 100%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.button .text-icon i,
.button .text-icon span{
  position: relative;
  color: #FF0000;
  font-size: 26px;
}
.button .text-icon span{
  font-size: 20px;
  font-weight: 400;
  margin-left: 8px;
}

</style>


</body>
</html>

