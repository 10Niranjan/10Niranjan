<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Niranjan Nitin Patil - Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 60px 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h1 {
            text-align: center;
            font-size: 3em;
            color: #2d3748;
            margin-bottom: 30px;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .wave {
            animation: wave 2s ease-in-out infinite;
            display: inline-block;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40% { transform: rotate(-4deg); }
            50% { transform: rotate(10deg); }
        }

        .typing-container {
            text-align: center;
            min-height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .typing-text {
            font-size: 1.4em;
            color: #1E90FF;
            font-weight: 500;
            font-family: 'Fira Code', 'Courier New', monospace;
            display: inline-block;
            border-right: 3px solid #1E90FF;
            padding-right: 8px;
            animation: blink 0.7s step-end infinite;
            white-space: nowrap;
            overflow: hidden;
        }

        @keyframes blink {
            from, to { border-color: transparent; }
            50% { border-color: #1E90FF; }
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 40px;
            animation: fadeInUp 1.2s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .skill-badge {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 24px;
            border-radius: 25px;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-badge:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.6);
        }

        @media (max-width: 768px) {
            .container {
                padding: 40px 20px;
            }

            h1 {
                font-size: 2em;
            }

            .typing-text {
                font-size: 1.1em;
            }

            .skill-badge {
                padding: 10px 20px;
                font-size: 0.9em;
            }
        }

        @media (max-width: 480px) {
            h1 {
                font-size: 1.5em;
            }

            .typing-text {
                font-size: 0.95em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hi <span class="wave">👋</span>, I'm Niranjan Nitin Patil</h1>
        
        <div class="typing-container">
            <div class="typing-text" id="typingText"></div>
        </div>

        <div class="skills-container">
            <div class="skill-badge">Java Developer</div>
            <div class="skill-badge">Flutter Developer</div>
            <div class="skill-badge">.NET Framework</div>
            <div class="skill-badge">Mobile Development</div>
            <div class="skill-badge">Web Development</div>
            <div class="skill-badge">Software Developer</div>
        </div>
    </div>

    <script>
        const texts = [
            "Java Developer | Flutter Developer",
            "Java • Flutter • .NET",
            "Mobile & Web Development Enthusiast",
            "Building Solutions with Java, Flutter & Modern Web Technologies",
            "Software Developer | .NET Framework"
        ];

        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingSpeed = 80;
        const deletingSpeed = 50;
        const pauseDuration = 2000;

        function type() {
            const currentText = texts[textIndex];
            const typingElement = document.getElementById('typingText');

            if (!isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;

                if (charIndex === currentText.length) {
                    isDeleting = true;
                    setTimeout(type, pauseDuration);
                    return;
                }
            } else {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;

                if (charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                    setTimeout(type, 500);
                    return;
                }
            }

            setTimeout(type, isDeleting ? deletingSpeed : typingSpeed);
        }

        // Start typing animation when page loads
        window.addEventListener('load', () => {
            setTimeout(type, 500);
        });
    </script>
</body>
</html>



### Java Developer | Flutter Developer | Java • Flutter • .NET | Mobile & Web Development Enthusiast | Building Solutions with Java, Flutter & Modern Web Technologies | Software Developer | .NET Framework

- 🌱 I'm currently learning **Spring Boot**

- 📫 How to reach me **pvt.niranjan10@gmail.com**

- 📄 Know about my experiences **[https://drive.google.com/file/d/1G4IfJMabq0bfUAGO1LTj8nfEJv0SBiDO/view?usp=drive_link](https://drive.google.com/file/d/1G4IfJMabq0bfUAGO1LTj8nfEJv0SBiDO/view?usp=drive_link)**


<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://github.com/10Niranjan" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg" alt="10Niranjan" height="30" width="40" /></a>
<a href="https://linkedin.com/in/niranjanpatil10" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="niranjanpatil10" height="30" width="40" /></a>
<a href="https://leetcode.com/niranjanpatil1683" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/leet-code.svg" alt="niranjanpatil1683" height="30" width="40" /></a>
</p>


<h3 align="left">Languages and Tools:</h3>
<p align="left">
<a href="https://developer.mozilla.org/en-US/docs/Web/android" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=androidstudio" alt="android" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/aws" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=aws" alt="aws" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/c" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=c" alt="c" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/cplusplus" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=cpp" alt="cplusplus" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/csharp" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=cs" alt="csharp" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/css3" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=css" alt="css3" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/dart" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=dart" alt="dart" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/dotnet" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=dotnet" alt="dotnet" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/figma" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=figma" alt="figma" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/flutter" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=flutter" alt="flutter" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/git" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=git" alt="git" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/html5" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=html" alt="html5" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/java" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=java" alt="java" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/javascript" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=js" alt="javascript" width="40" height="40"/> </a>
<a href="https://developer.mozilla.org/en-US/docs/Web/linux" target="_blank" rel="noreferrer"> <img src="https://skillicons.dev/icons?i=linux" alt="linux" width="40" height="40"/> </a>
</p>


