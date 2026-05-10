# Letterboxd Survey Form - HTML Certification Project

## Project Overview

This project is my first HTML certification submission for the freeCodeCamp HTML course. The task required me to build a functional survey form following specific requirements while incorporating my own creative design and theme. I created a **Letterboxd Profile Survey Form** — an interactive form designed to gather user feedback and preferences from the Letterboxd community.

## Why Letterboxd?

I chose to build a survey form around **Letterboxd** because it's a beloved and vibrant social platform that connects film enthusiasts worldwide. Letterboxd allows users to:
- Rate and review films they've watched
- Discover movies through community recommendations
- Build and organize personal watchlists
- Connect with like-minded film lovers
- Document their viewing history

As someone interested in both technology and media consumption patterns, Letterboxd represented the perfect subject for a survey form. Collecting feedback from users about their experience with the platform would provide valuable insights into user preferences, satisfaction levels, and feature requests.

## What The Form Collects

The survey form gathers information in several categories:

### Personal Information
- **Name & Email**: Core identification fields (required)
- **Age**: Optional demographic data with validation (16-99 years)

### Content Preferences
- A dropdown to capture users' preferred media type (Film, TV Series, Anime, Cartoon, Documentary, News)
- Understanding what content users consume most helps identify usage patterns

### Platform Engagement
- A radio button group asking whether users would recommend Letterboxd to friends
- A dropdown menu capturing what users like most about Letterboxd (Reviews, Ratings, Following friends, Organizing watchlists, Four Favorites, Community)

### Feature Requests
- A checkbox group for improvements users want to see (Threaded comments, TV show support, Advanced filtering, Better design, AI recommendations, etc.)
- An optional text area for additional comments and suggestions

## Technical Implementation

### HTML Elements Used

**Form Structure:**
- `<form>` - Container for all form elements
- Proper `id` attributes for form validation and styling

**Input Types:**
- `<input type="text">` - For name entry
- `<input type="email">` - For email validation
- `<input type="number">` - For age with min/max constraints
- `<input type="radio">` - For mutually exclusive options
- `<input type="checkbox">` - For multiple selections

**Selection Elements:**
- `<select>` and `<option>` - For dropdown menus with predefined choices

**Text Input:**
- `<textarea>` - For longer open-ended feedback

**Form Control:**
- `<button>` - Submit button to complete the form

**Semantic Structure:**
- `<label>` elements properly associated with form inputs
- `<h1>` for the main title
- `<p>` for description text
- `<br>` tags for visual spacing

### Key Attributes Implemented

- **required** - Makes name and email mandatory fields
- **placeholder** - Provides helpful hints for users
- **min/max** - Validates numeric input (age between 16-99)
- **name** - Groups radio buttons so only one can be selected at a time
- **value** - Associates data with each option
- **lang="en"** - Specifies document language
- **charset="UTF-8"** - Ensures proper character encoding

## What I Learned

### 1. **Form Accessibility & UX**
I learned the importance of:
- Properly using `<label>` elements for accessibility
- Providing clear placeholder text to guide users
- Grouping related form elements logically
- Using appropriate input types for better user experience on different devices (email keyboards, numeric keyboards)

### 2. **HTML Form Structure**
- How to create semantic and well-organized forms
- The difference between various input types and when to use each
- How radio buttons require the same `name` attribute to function as mutually exclusive options
- How checkboxes allow multiple selections while radio buttons don't

### 3. **Data Collection Strategy**
- Designing forms to gather meaningful data requires thoughtful question ordering
- Mix of required and optional fields affects completion rates
- Multiple-choice options (dropdowns, radio buttons, checkboxes) provide better data quality than free text

### 4. **HTML Best Practices**
- Proper document structure with DOCTYPE, html, head, and body tags
- Meta tags for charset declaration
- Meaningful ID attributes for form control and future JavaScript/CSS targeting
- Self-closing vs. closing tags (though I should note that in HTML5, the closing `</input>` tags in my code are not necessary as `<input />` is self-closing)

### 5. **Real-World Application Design**
- Survey forms aren't just technical exercises — they're tools for gathering real feedback
- Choosing a familiar platform (Letterboxd) made it easier to design relevant questions
- Forms should be user-friendly, not overwhelming

## Challenges Overcome

1. **Balancing Required vs. Optional Fields** - Deciding which information was truly necessary
2. **Question Order** - Arranging questions logically to improve completion flow
3. **Option Variety** - Creating relevant dropdown and checkbox options without overwhelming users
4. **Semantic HTML** - Ensuring proper label-input associations for accessibility

## Future Enhancements

If this project were to be expanded, I would add:
- CSS styling for better visual design
- JavaScript validation and feedback
- Backend integration for data storage
- Conditional questions that appear based on previous answers
- Better mobile responsiveness

## Key Takeaways

This project reinforced that **HTML forms are the foundation of user interaction on the web**. While seemingly simple, creating an effective form requires understanding user needs, proper semantic structure, and attention to accessibility. By building a form around a real platform like Letterboxd, I could appreciate how forms connect directly to product feedback and user experience improvement.



## Code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Survey Form</title>
  </head>
    
  <body>   
    <h1 id="title">LETTERBOXD PROFILE FORM</h1>
    <p id="description">Thank you for taking part of this research. Tell us a little bit about you and your passion for movies in this form.</p>

    <form id="survey-form">
      
      <label id="name-label">Name
        <input id="name" type="text" placeholder="Enter your name" required>
        <br>
      </label>

      <label id="email-label">Email
        <input id="email" type="email" placeholder="Enter your email" required>
        <br>
      </label>

      <label id="number-label">Age (optional)
        <input id="number" type="number" min="16" max="99" placeholder="Age">
      </label>

      <br>
      <br>

      <label>Which of the following options is your favorite to consume:
        <br>
        <select id="dropdown-media">
          <option value="Film">Film</option>
          <option value="TV Series">TV Series</option>
          <option value="Anime">Anime</option>
          <option value="Cartoon">Cartoon</option>
          <option value="Documentary">Documentary</option>
          <option value="News">News</option>
        </select>
      </label>

      <br>
      <br>

      <label id="opinion">Would you recommend Letterboxd to a friend?
      </label>
      
      <br>
      
      <input type="radio" name="option" value="Yeah, definitely"> Yeah, definitely
      <input type="radio" name="option" value="Maybe"> Maybe
      <input type="radio" name="option" value="Not sure"> Not sure

      <br>
      <br>
      
      <label>What do you like the most in Letterboxd?
        <br>
        <select id="dropdown-features">
          <option value="Reviews">Reviews</option>
          <option value="Rating movies">Rating movies</option>
          <option value="Following friends">Following friends</option>
          <option value="Organizing watchlist">Organizing watchlist</option>
          <option value="Four Favorites">Four Favorites</option>
          <option value="Community">Community</option>
        </select>
      </label>

      <br>
      <br>

      <label id="improvements">What would you like to see new? (Check all that apply)
        <br>  
        
        <input type="checkbox" value="Threaded comments"> Threaded comments
        <input type="checkbox" value="TV show support"> TV show support
        <input type="checkbox" value="Advanced filtering"> Advanced filtering
        <input type="checkbox" value="Better design"> Better design
        <input type="checkbox" value="Personalized AI recommendations"> Personalized AI recommendations
        <input type="checkbox" value="Log other types of media"> Log other types of media
      </label>

      <br>
      <br>

      <label id="suggestions">Any comments or suggestions?</label>

      <br>

      <textarea id="comments" placeholder="Enter your comment here..."></textarea>
      <br>
      <button id="submit">Submit</button>

    </form>
    
  </body>
</html>
