# 🌙 Neon Bar Profile Widget

Add a dynamic cocktail glass and a level-up bartender cat to your GitHub profile README. Link with your GitHub Stars count automatically!

<div align="center">
  <table style="border: none; border-collapse: collapse;">
    <tr style="border: none;">
      <td align="center" style="border: none; padding: 10px;">
        <img src="assets/cocktail.svg?v=1784709485952" width="280" alt="Cocktail Glass" />
      </td>
      <td align="center" style="border: none; padding: 10px;">
        <img src="assets/cat_bartender.svg?v=1784709485952" width="280" alt="Bartender Cat" />
      </td>
    </tr>
  </table>
</div>

## ✨ Features

*   **Dynamic Cocktail Glass**: The level of the cocktail liquid automatically rises based on your total GitHub stars (Target: 200 stars).
*   **Level-up Bartender Cat**: The cat bartender upgrades its outfit, accessories (like neon sunglasses, crowns, etc.), and title as your stars grow.
*   **Today's Special Drink**: Displays a recommended cocktail corresponding to your current star level!
*   **Fully Automated**: Updates automatically every 6 hours using GitHub Actions. No manual work required.
*   **Cache-Buster Support**: Includes an automatic timestamp parameter update to bypass GitHub's image cache, ensuring you always see the latest visual state.

---

## 🍹 Cocktail & Bartender Level System

Depending on your total stars count, the cocktail drink and the cat bartender's rank will upgrade:

| Stars Count | 🍸 Today's Special Drink | 🐱 Cat Bartender Title & Gear |
| :--- | :--- | :--- |
| **0 ~ 49** | `Blue Hawaii` | `Lv.1 Apprentice Cat` (Looking confused with an empty shaker ❓) |
| **50 ~ 99** | `Tequila Sunrise` | `Lv.2 Adept Mixologist` (Vigorously shaking the drink ⚡) |
| **100 ~ 149** | `Martini` | `Lv.3 Master Mixologist` (Rocking neon red sunglasses! 😎) |
| **150 ~ 199** | `Cosmopolitan` | `Lv.4 Legendary Bartender` (Wearing a shiny neon crown 👑) |
| **200+** | `CatMoon Special` | `Lv.5 Cosmic Mixologist` (Equipped with a space helmet under shooting stars 🌠) |

---

## 🚀 Quick Setup (How to Use)

You can set this up on your GitHub profile README in just 3 easy steps!

### Step 1: Fork this Repository
Click the **Fork** button at the top right of this page to copy this repository to your own GitHub account.

### Step 2: Enable Workflow Permissions
To allow the widget to automatically update the images and your README, you need to grant write permissions to GitHub Actions:
1.  Go to your forked repository's **Settings** tab.
2.  Click on **Actions** > **General** in the left sidebar.
3.  Scroll down to **Workflow permissions**, select **Read and write permissions**, and click **Save**.
4.  Go to the **Actions** tab of your repository, select **Generate Cocktail Star Glass** workflow, and click **Enable workflow**.

### Step 3: Add the Widget to your Profile README
Open your profile README (the repository named after your username) and insert the following code where you want the bar to appear. 
*(Be sure to replace `YOUR_USERNAME` with your actual GitHub username in three places)*

```html
<div align="center">
  <table style="border: none; border-collapse: collapse;">
    <tr style="border: none;">
      <td align="center" style="border: none; padding: 10px;">
        <img src="https://raw.githubusercontent.com/YOUR_USERNAME/neon-bar-profile/main/assets/cocktail.svg?v=1784709485952" width="300" alt="Cocktail Glass" />
      </td>
      <td align="center" style="border: none; padding: 10px;">
        <img src="https://raw.githubusercontent.com/YOUR_USERNAME/neon-bar-profile/main/assets/cat_bartender.svg?v=1784709485952" width="300" alt="Bartender Cat" />
      </td>
    </tr>
  </table>
</div>
```

If you want to add a cool **Opening Hours (Active Hours)** card underneath the bar, you can copy this styled text block as well:

```html
<div align="center">
  <h3>🕒 Opening Hours</h3>
  
  **Weekdays (Mon - Fri)**: 18:00 - 24:00 (Night shift bartender 🌃)
  <br>
  **Weekends (Sat - Sun)**: 10:00 - 22:00 (Always at the bar ☀️)
  <br>
  **Closed**: When all bugs are resolved (Practically open every day 🧪)
  <br>
  **Orders (Contact)**: your.email@example.com (Or check the SNS badges below 🚪)
</div>
```

---

## 🛠️ Local Testing / Development

To generate the SVG images manually, clone the repository locally and run:

```bash
node scripts/generate_cocktail.js
```

The script will fetch your stars count and update the assets inside the `assets/` folder.
