# week-6-assigment
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Future of AI & Learning</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body class="p-4 sm:p-8">

    <div class="max-w-5xl mx-auto bg-white p-6 rounded-lg shadow-xl">

        <h1 class="text-3xl sm:text-4xl font-bold text-center text-indigo-700 mb-6">Exploring the Future of AI & How to Learn It</h1>

        <p id="aiIntroText" class="text-lg text-center mb-8 text-gray-700">Artificial Intelligence is shaping our world. Discover what's next and find the resources to start your AI journey.</p>

        <div class="text-center my-8">
            <button id="infoButton" class="px-6 py-3 bg-blue-600 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 transition-colors duration-300">Reveal a Learning Tip</button>
            <div id="learningTip" class="mt-4 p-4 bg-yellow-100 border-l-4 border-yellow-500 text-yellow-800 hidden rounded-md">
                </div>
        </div>

        <div class="my-10">
            <h2 class="text-2xl font-semibold text-center text-gray-800 mb-6">AI in Action: Image Gallery</h2>
            <div id="galleryContainer" class="relative w-full max-w-2xl mx-auto overflow-hidden rounded-lg shadow-lg">
                <img id="galleryImage" src="https://placehold.co/800x400/a78bfa/ffffff?text=AI+Concept+1" alt="AI Concept Image" class="w-full h-auto transition-opacity duration-500 ease-in-out opacity-100">
                <button id="prevImage" class="absolute top-1/2 left-4 transform -translate-y-1/2 bg-black bg-opacity-50 text-white p-2 rounded-full focus:outline-none hover:bg-opacity-75 transition-opacity duration-300">&lt;</button>
                <button id="nextImage" class="absolute top-1/2 right-4 transform -translate-y-1/2 bg-black bg-opacity-50 text-white p-2 rounded-full focus:outline-none hover:bg-opacity-75 transition-opacity duration-300">&gt;</button>
            </div>
        </div>

        <div class="my-10">
            <h2 class="text-2xl font-semibold text-center text-gray-800 mb-6">Learning Paths & Tools</h2>

            <div id="tabsContainer" class="hidden md:block border-b border-gray-200">
                <nav class="-mb-px flex space-x-8" aria-label="Tabs">
                    <button class="tab-button py-4 px-1 text-center border-b-2 font-medium text-sm focus:outline-none transition-colors duration-200 ease-in-out text-indigo-600 border-indigo-500" data-tab="overview">Overview</button>
                    <button class="tab-button py-4 px-1 text-center border-b-2 font-medium text-sm focus:outline-none transition-colors duration-200 ease-in-out border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300" data-tab="basics">Basics</button>
                    <button class="tab-button py-4 px-1 text-center border-b-2 font-medium text-sm focus:outline-none transition-colors duration-200 ease-in-out border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300" data-tab="tools">Key Tools</button>
                    <button class="tab-button py-4 px-1 text-center border-b-2 font-medium text-sm focus:outline-none transition-colors duration-200 ease-in-out border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300" data-tab="resources">Resources</button>
                </nav>
            </div>

            <div id="accordionContainer" class="md:hidden">
                </div>

            <div id="tabContent" class="mt-6">
                <div class="tab-pane" id="overview" data-tab-content>
                    <h3 class="text-xl font-semibold mb-3">AI Learning Overview</h3>
                    <p>Start with the fundamentals of programming (Python recommended), then dive into linear algebra, calculus, and statistics. Understand machine learning concepts before exploring deep learning and specialized fields.</p>
                </div>
                <div class="tab-pane hidden" id="basics" data-tab-content>
                     <h3 class="text-xl font-semibold mb-3">Getting Started: The Basics</h3>
                    <p>Learn Python, data structures, and algorithms. Familiarize yourself with libraries like NumPy and Pandas for data manipulation. Understand core ML concepts like supervised vs. unsupervised learning.</p>
                </div>
                 <div class="tab-pane hidden" id="tools" data-tab-content>
                    <h3 class="text-xl font-semibold mb-3">Essential AI Tools & Libraries</h3>
                    <p>Key tools include TensorFlow, PyTorch (deep learning frameworks), Scikit-learn (machine learning), and Jupyter Notebooks (interactive development). Cloud platforms like AWS, Google Cloud, and Azure offer AI services.</p>
                </div>
                 <div class="tab-pane hidden" id="resources" data-tab-content>
                    <h3 class="text-xl font-semibold mb-3">Further Learning Resources</h3>
                    <p>Explore online courses (Coursera, edX, Udacity), documentation for libraries, research papers, and community forums (Stack Overflow, Reddit communities). Practice with datasets on platforms like Kaggle.</p>
                </div>
            </div>
        </div>


        <div class="my-10 p-6 bg-gray-50 rounded-lg shadow-inner">
            <h2 class="text-2xl font-semibold text-center text-gray-800 mb-6">Sign Up for AI Learning Updates</h2>
            <form id="signupForm" class="max-w-md mx-auto">
                <div class="mb-4">
                    <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email Address:</label>
                    <input type="email" id="email" name="email" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                    <p id="emailError" class="text-red-500 text-xs italic mt-1 hidden">Please enter a valid email address.</p>
                </div>
                <div class="mb-6">
                    <label for="password" class="block text-gray-700 text-sm font-bold mb-2">Password:</label>
                    <input type="password" id="password" name="password" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" required minlength="8">
                    <p id="passwordError" class="text-red-500 text-xs italic mt-1 hidden">Password must be at least 8 characters long and include a number and special character.</p>
                </div>
                 <div class="mb-6">
                    <label for="confirmPassword" class="block text-gray-700 text-sm font-bold mb-2">Confirm Password:</label>
                    <input type="password" id="confirmPassword" name="confirmPassword" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" required minlength="8">
                    <p id="confirmPasswordError" class="text-red-500 text-xs italic mt-1 hidden">Passwords do not match.</p>
                </div>
                <div class="flex items-center justify-between">
                    <button type="submit" class="bg-purple-600 hover:bg-purple-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline transition-colors duration-300">
                        Sign Up
                    </button>
                </div>
                 <p id="formSuccess" class="text-green-500 text-center mt-4 hidden">Thank you for signing up!</p>
            </form>
        </div>

        <div id="secretArea" class="mt-10 p-6 bg-pink-100 border border-dashed border-pink-400 rounded-lg text-center cursor-pointer">
            <p class="text-pink-800">Double-click or Long Press here for a secret AI resource!</p>
            <div id="secretContent" class="mt-4 text-pink-700 font-semibold hidden">
                <p>🤫 Secret Resource Unlocked! Check out: <a href="https://research.google/" target="_blank" class="text-pink-900 underline hover:no-underline">Google AI Research</a></p>
            </div>
        </div>


    </div>

    <script src="script.js"></script>

</body>
</html>
/* Base styles */
body {
    font-family: 'Inter', sans-serif; /* Use Inter font */
    background-color: #f4f7f6; /* Light background */
    color: #333;
    line-height: 1.6;
}

/* Custom styles for the added learning tip */
#learningTip {
    opacity: 0; /* Start hidden */
    transform: translateY(20px); /* Start slightly below */
    transition: opacity 0.5s ease-out, transform 0.5s ease-out;
}

#learningTip.visible {
    opacity: 1;
    transform: translateY(0);
}

/* Styles for the image gallery */
#galleryImage {
    max-height: 400px; /* Limit image height */
    object-fit: cover; /* Ensure image covers the area without distortion */
}

/* Styles for tabs */
.tab-button {
    cursor: pointer;
}

.tab-button[data-tab].text-indigo-600 {
    border-color: #6366f1; /* Active tab color */
}

/* Styles for accordion */
.accordion-item {
    border: 1px solid #e5e7eb; /* Tailwind gray-200 */
    margin-bottom: 8px; /* Tailwind mb-2 */
    border-radius: 4px; /* Tailwind rounded */
    overflow: hidden;
}

.accordion-header {
    background-color: #f9fafb; /* Tailwind gray-50 */
    padding: 12px 16px; /* Tailwind p-3 p-4 */
    cursor: pointer;
    font-weight: 600; /* Tailwind font-semibold */
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.accordion-content {
    padding: 16px; /* Tailwind p-4 */
    background-color: #fff;
    display: none; /* Hidden by default */
    border-top: 1px solid #e5e7eb;
}

.accordion-content.active {
    display: block; /* Show when active */
}

.accordion-icon {
    transition: transform 0.3s ease;
}

.accordion-icon.rotate {
    transform: rotate(180deg);
}


/* Styles for form validation feedback */
input:invalid:not(:placeholder-shown) {
    border-color: #ef4444; /* Tailwind red-500 */
}

input:valid:not(:placeholder-shown) {
     border-color: #22c55e; /* Tailwind green-500 */
}

#emailError, #passwordError, #confirmPasswordError {
    /* Styles already set in HTML with Tailwind classes */
}

/* Animation for form success message */
#formSuccess {
    opacity: 0;
    transition: opacity 0.5s ease-out;
}

#formSuccess.visible {
    opacity: 1;
}

/* Styles for the secret area */
#secretArea {
    transition: background-color 0.3s ease;
}

#secretArea:hover {
    background-color: #ffe4e6; /* Lighter pink on hover */
}

#secretContent {
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.5s ease-out, transform 0.5s ease-out;
}

#secretContent.visible {
    opacity: 1;
    transform: translateY(0);
}

// Wait for the DOM to be fully loaded before running the script
document.addEventListener('DOMContentLoaded', () => {

    // --- Event Handling & Dynamic Content ---
    const infoButton = document.getElementById('infoButton');
    const learningTipElement = document.getElementById('learningTip');
    const aiIntroTextElement = document.getElementById('aiIntroText'); // Get the intro text element

    const learningTips = [
        "Tip: Start with Python! It's the most popular language for AI and Machine Learning.",
        "Tip: Don't be afraid of the math. Linear algebra, calculus, and statistics are key.",
        "Tip: Practice with real datasets on platforms like Kaggle.",
        "Tip: Follow AI researchers and communities online to stay updated.",
        "Tip: Build small projects to apply what you learn."
    ];
    let currentTipIndex = 0;

    // Button click event
    infoButton.addEventListener('click', () => {
        // Display the next learning tip
        learningTipElement.textContent = learningTips[currentTipIndex];
        learningTipElement.classList.remove('hidden'); // Make it visible
        // Trigger animation by adding/removing a class after a small delay
        setTimeout(() => {
             learningTipElement.classList.add('visible');
        }, 10); // Small delay to allow display:block to apply

        currentTipIndex = (currentTipIndex + 1) % learningTips.length; // Cycle through tips
    });

    // Keypress detection (Example: Change intro text on 'A' key)
    document.addEventListener('keypress', (event) => {
        if (event.key === 'a' || event.key === 'A') {
            aiIntroTextElement.textContent = "KeyPress detected! Focus on learning fundamentals for AI!";
             // Reset after a few seconds
            setTimeout(() => {
                aiIntroTextElement.textContent = "Artificial Intelligence is shaping our world. Discover what's next and find the resources to start your AI journey.";
            }, 3000);
        }
    });

    // Secret Action: Double-click or Long Press
    const secretArea = document.getElementById('secretArea');
    const secretContent = document.getElementById('secretContent');
    let pressTimer;

    // Double-click event
    secretArea.addEventListener('dblclick', () => {
        secretContent.classList.remove('hidden');
        setTimeout(() => {
            secretContent.classList.add('visible');
        }, 10);
    });

    // Long press simulation (using mousedown/touchstart and mouseup/touchend)
    secretArea.addEventListener('mousedown', startPress, false);
    secretArea.addEventListener('touchstart', startPress, false); // For touch devices
    secretArea.addEventListener('mouseup', cancelPress, false);
    secretArea.addEventListener('touchend', cancelPress, false); // For touch devices
    secretArea.addEventListener('mouseleave', cancelPress, false); // Cancel if mouse leaves area

    function startPress() {
        // Clear any existing timer
        cancelPress();
        // Start a new timer for 1 second (1000 ms)
        pressTimer = setTimeout(() => {
            // Action for long press
            secretContent.classList.remove('hidden');
             setTimeout(() => {
                secretContent.classList.add('visible');
            }, 10);
        }, 1000); // 1 second long press
    }

    function cancelPress() {
        clearTimeout(pressTimer);
    }


    // --- Interactive Elements ---

    // Image Gallery/Slideshow
    const galleryImage = document.getElementById('galleryImage');
    const prevImageButton = document.getElementById('prevImage');
    const nextImageButton = document.getElementById('nextImage');

    const galleryImages = [
        { src: 'https://placehold.co/800x400/a78bfa/ffffff?text=AI+Concept+1', alt: 'AI Concept 1' },
        { src: 'https://placehold.co/800x400/60a5fa/ffffff?text=Machine+Learning', alt: 'Machine Learning' },
        { src: 'https://placehold.co/800x400/34d399/ffffff?text=Neural+Network', alt: 'Neural Network' },
        { src: 'https://placehold.co/800x400/facc15/ffffff?text=Data+Science', alt: 'Data Science' }
    ];
    let currentImageIndex = 0;

    function updateGalleryImage() {
        // Add a class to start fade out
        galleryImage.classList.remove('opacity-100');
        galleryImage.classList.add('opacity-0');

        // Wait for fade out transition to complete before changing src
        setTimeout(() => {
            galleryImage.src = galleryImages[currentImageIndex].src;
            galleryImage.alt = galleryImages[currentImageIndex].alt;
             // Remove fade out class and add fade in
            galleryImage.classList.remove('opacity-0');
            galleryImage.classList.add('opacity-100');
        }, 500); // Match CSS transition duration
    }

    prevImageButton.addEventListener('click', () => {
        currentImageIndex = (currentImageIndex - 1 + galleryImages.length) % galleryImages.length;
        updateGalleryImage();
    });

    nextImageButton.addEventListener('click', () => {
        currentImageIndex = (currentImageIndex + 1) % galleryImages.length;
        updateGalleryImage();
    });


    // Tabs / Accordion
    const tabButtons = document.querySelectorAll('.tab-button');
    const tabPanes = document.querySelectorAll('.tab-pane');
    const accordionContainer = document.getElementById('accordionContainer');
    const tabContentContainer = document.getElementById('tabContent');

    // Generate Accordion items from tab content for small screens
    tabPanes.forEach(pane => {
        const headerText = pane.querySelector('h3').textContent;
        const contentHTML = pane.innerHTML; // Get full content including h3

        const accordionItem = document.createElement('div');
        accordionItem.classList.add('accordion-item');

        const accordionHeader = document.createElement('div');
        accordionHeader.classList.add('accordion-header');
        accordionHeader.innerHTML = `<span>${headerText}</span><i class="fas fa-chevron-down accordion-icon"></i>`; // Add icon

        const accordionContent = document.createElement('div');
        accordionContent.classList.add('accordion-content');
        accordionContent.innerHTML = contentHTML; // Use full content

        accordionItem.appendChild(accordionHeader);
        accordionItem.appendChild(accordionContent);
        accordionContainer.appendChild(accordionItem);

        // Add click listener to accordion header
        accordionHeader.addEventListener('click', () => {
            // Close other accordion items
            document.querySelectorAll('.accordion-content.active').forEach(item => {
                if (item !== accordionContent) {
                    item.classList.remove('active');
                    item.previousElementSibling.querySelector('.accordion-icon').classList.remove('rotate');
                }
            });

            // Toggle active state for the clicked item
            accordionContent.classList.toggle('active');
            accordionHeader.querySelector('.accordion-icon').classList.toggle('rotate');
        });
    });


    // Tab functionality for larger screens
    tabButtons.forEach(button => {
        button.addEventListener('click', () => {
            const targetTab = button.dataset.tab;

            // Deactivate all tabs and hide all panes
            tabButtons.forEach(btn => {
                btn.classList.remove('text-indigo-600', 'border-indigo-500');
                btn.classList.add('border-transparent', 'text-gray-500', 'hover:text-gray-700', 'hover:border-gray-300');
            });
            tabPanes.forEach(pane => {
                pane.classList.add('hidden');
            });

            // Activate the clicked tab and show the target pane
            button.classList.add('text-indigo-600', 'border-indigo-500');
            button.classList.remove('border-transparent', 'text-gray-500', 'hover:text-gray-700', 'hover:border-gray-300');
            document.getElementById(targetTab).classList.remove('hidden');
        });
    });


    // --- Form Validation ---
    const signupForm = document.getElementById('signupForm');
    const emailInput = document.getElementById('email');
    const passwordInput = document.getElementById('password');
    const confirmPasswordInput = document.getElementById('confirmPassword');
    const emailError = document.getElementById('emailError');
    const passwordError = document.getElementById('passwordError');
    const confirmPasswordError = document.getElementById('confirmPasswordError');
    const formSuccessMessage = document.getElementById('formSuccess');

    // Function to validate email format
    function isValidEmail(email) {
        // Simple regex for email format validation
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        return emailRegex.test(email);
    }

     // Function to validate password complexity (min 8 chars, includes number and special char)
    function isValidPassword(password) {
        const minLength = 8;
        const hasNumber = /[0-9]/.test(password);
        const hasSpecialChar = /[!@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?]+/.test(password);
        return password.length >= minLength && hasNumber && hasSpecialChar;
    }


    // Real-time validation feedback on input change/blur
    emailInput.addEventListener('input', validateEmail);
    emailInput.addEventListener('blur', validateEmail); // Also validate when focus leaves

    passwordInput.addEventListener('input', validatePassword);
    passwordInput.addEventListener('blur', validatePassword);

    confirmPasswordInput.addEventListener('input', validateConfirmPassword);
    confirmPasswordInput.addEventListener('blur', validateConfirmPassword);


    function validateEmail() {
        if (emailInput.value.trim() === '') {
            emailError.textContent = 'Email address is required.';
            emailError.classList.remove('hidden');
            return false;
        } else if (!isValidEmail(emailInput.value)) {
            emailError.textContent = 'Please enter a valid email address.';
            emailError.classList.remove('hidden');
            return false;
        } else {
            emailError.classList.add('hidden');
            return true;
        }
    }

    function validatePassword() {
         if (passwordInput.value.trim() === '') {
            passwordError.textContent = 'Password is required.';
            passwordError.classList.remove('hidden');
             return false;
        } else if (!isValidPassword(passwordInput.value)) {
            passwordError.textContent = 'Password must be at least 8 characters, include a number and special character.';
            passwordError.classList.remove('hidden');
             return false;
        } else {
            passwordError.classList.add('hidden');
             return true;
        }
    }

     function validateConfirmPassword() {
         if (confirmPasswordInput.value.trim() === '') {
            confirmPasswordError.textContent = 'Please confirm your password.';
            confirmPasswordError.classList.remove('hidden');
             return false;
        } else if (confirmPasswordInput.value !== passwordInput.value) {
            confirmPasswordError.textContent = 'Passwords do not match.';
            confirmPasswordError.classList.remove('hidden');
             return false;
        } else {
            confirmPasswordError.classList.add('hidden');
             return true;
        }
    }


    // Form submission handling
    signupForm.addEventListener('submit', (event) => {
        event.preventDefault(); // Prevent default form submission

        // Perform validation on submit
        const isEmailValid = validateEmail();
        const isPasswordValid = validatePassword();
        const isConfirmPasswordValid = validateConfirmPassword();

        // If all fields are valid
        if (isEmailValid && isPasswordValid && isConfirmPasswordValid) {
            // Simulate form submission success
            console.log('Form submitted successfully!');
            console.log('Email:', emailInput.value);
            console.log('Password:', passwordInput.value);

            // Show success message
            formSuccessMessage.classList.remove('hidden');
             setTimeout(() => {
                formSuccessMessage.classList.add('visible');
            }, 10);


            // Reset the form (optional)
            signupForm.reset();

            // Hide error messages after successful submission
            emailError.classList.add('hidden');
            passwordError.classList.add('hidden');
            confirmPasswordError.classList.add('hidden');

             // Hide success message after a few seconds
            setTimeout(() => {
                 formSuccessMessage.classList.remove('visible');
                 setTimeout(() => {
                     formSuccessMessage.classList.add('hidden');
                 }, 500); // Match CSS transition duration
            }, 5000); // Show for 5 seconds

        } else {
            console.log('Form validation failed.');
            // Error messages are already shown by the validation functions
        }
    });

}); // End of DOMContentLoaded listener
