## Step-by-Step Guide: Creating a Responsive Web Page with Team Profiles

### Step 1: Set Up Your Development Environment

#### 1. **Download and Install VS Code**
   - Go to the official [VS Code website](https://code.visualstudio.com/) and download the version for your operating system (Windows, Mac, Linux).
   - Install it on your machine following the instructions.

#### 2. **Install Live Server Extension (Optional)**
   - Open VS Code.
   - Go to the **Extensions** tab on the left sidebar (or press `Ctrl+Shift+X`).
   - Search for `Live Server` by Ritwick Dey and click **Install**. 
   - This allows you to preview your web page live as you make changes.

---

### Step 2: Create the Project Folder and Files

#### 1. **Create the Folder Structure**
   - Open **VS Code**.
   - Select **File > Open Folder...** and choose a location on your computer where you'd like to save your project (e.g., Desktop).
   - Create a new folder named `team-profile-project`.
   
#### 2. **Inside VS Code, Create the Project Files**
   - **In VS Code**, open the **Explorer** tab (or press `Ctrl+Shift+E`).
   - **Right-click** the `team-profile-project` folder and choose **New File**.
   - Create the following files and folders:

     - `index.html` (Main HTML file)
     - `styles/` (Folder for the CSS file)
     - Inside the `styles/` folder, create `style.css` (The CSS file)
     - `images/` (Folder for team member images)

#### 3. **Add Placeholder Images**
   - For each team member, you can use a placeholder image. You can either download actual images and place them in the `images` folder, or use a placeholder URL like:
   
     - [Placeholder.com](https://placeholder.com) or [lorem picsum](https://picsum.photos/) to generate placeholder images.
   - If you download images, make sure they are saved in the `images/` folder, e.g., `profile1.jpg`, `profile2.jpg`, etc.

---

### Step 3: Write the HTML Code

1. **Open `index.html`** inside VS Code and paste the following HTML code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meet Our Team</title>
    <link rel="stylesheet" href="styles/style.css">
</head>
<body>
    <!-- Header Section -->
    <header>
        <h1>Meet Our Team</h1>
    </header>

    <!-- Team Profiles Section -->
    <section class="team-section">
        <!-- Team Member 1 -->
        <div class="team-member">
            <img src="images/profile1.jpg" alt="Team Member 1">
            <h2>John Doe</h2>
            <p>Software Engineer</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
        <!-- Team Member 2 -->
        <div class="team-member">
            <img src="images/profile2.jpg" alt="Team Member 2">
            <h2>Jane Smith</h2>
            <p>Product Manager</p>
            <p>Phasellus vel turpis egestas, semper metus in, laoreet justo.</p>
        </div>
        <!-- Add more team members here -->
    </section>

    <!-- Footer Section -->
    <footer>
        <p>Created by Team XYZ</p>
    </footer>
</body>
</html>
```

#### 2. **Explanation of the HTML Code**:
   - **`<header>`**: Contains the page title "Meet Our Team".
   - **`<section class="team-section">`**: This is where each team member's profile is displayed. You can add more profiles by copying the structure of each team member and modifying the details (image, name, title, and bio).
   - **`<footer>`**: Contains a simple footer message.

---

### Step 4: Write the CSS Code

1. **Open `styles/style.css`** and paste the following CSS code:

```css
/* Base styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

/* Header styling */
header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px 0;
}

/* Team section styling */
.team-section {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
    gap: 20px;
}

.team-member {
    background-color: white;
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    width: 300px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Image styling - Circular and responsive */
.team-member img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
}

/* Footer styling */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: relative;
    bottom: 0;
    width: 100%;
}
```

#### 2. **Explanation of the CSS Code**:
   - **Body styling**: Sets basic styling for the entire page with `Arial` font, `background-color`, and a margin reset for consistency.
   - **Header**: Gives the header a background color (`#333`), white text, and centers the text.
   - **Team Profiles Layout**: Uses **Flexbox** to center the team members and wrap them when necessary for responsive layout. Each `.team-member` has a background, padding, and box shadow for a card-like effect.
   - **Image styling**: Ensures team member images are circular by using `border-radius: 50%`, and sets `object-fit: cover` to maintain the aspect ratio.

---

### Step 5: Add Placeholder Images or Download Your Own

If you want to use placeholder images for your team members, you can use this placeholder URL in your HTML:

```html
<img src="https://via.placeholder.com/150" alt="Team Member">
```

Or, if you have your own images:
   - Download the images and save them inside the `images/` folder.
   - Make sure the filenames match what’s referenced in the HTML (`profile1.jpg`, `profile2.jpg`, etc.).

---

### Step 6: Add Responsive Design with Media Queries (Optional)

To make sure the page looks good on mobile and tablets, use **media queries**. Add this at the bottom of your `styles/style.css`:

```css
/* For tablets and smaller devices */
@media (max-width: 768px) {
    .team-member {
        width: 100%;
        max-width: 400px;
    }
}

/* For mobile devices */
@media (max-width: 480px) {
    h1 {
        font-size: 24px;
    }
    .team-member {
        padding: 10px;
    }
    .team-member img {
        width: 100px;
        height: 100px;
    }
}
```

### Explanation:
   - **Media queries**: This changes the layout and styling based on the screen size.
   - **Tablets (max-width: 768px)**: Team members will now stretch to fit a larger width on smaller screens like tablets.
   - **Mobile (max-width: 480px)**: The font sizes and image sizes are reduced for better readability on phones.

---

### Step 7: Preview the Project

1. **If you installed Live Server**:
   - Right-click on `index.html` inside VS Code and select **Open with Live Server**.
   - A new browser tab will open with your webpage, and you can see changes live as you edit the code.

2. **Without Live Server**:
   - Open your project folder in **File Explorer** (or Finder on Mac).
   - **Double-click** on `index.html`, and it will open in your browser.

---

### Step 8: Final Testing on Devices

To test how responsive your page is:
   - **Right-click** on the webpage in your browser and choose **Inspect** (or press `Ctrl+Shift+I`).
   - In the DevTools panel, click the **device toolbar** icon to simulate different screen sizes (mobile, tablet, desktop).

---
