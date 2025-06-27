---
applyTo: 03-ajax-to-fetch/**
---

# 🌐 From $.ajax to Fetch API

When the user types "start the training":

1. **Start with jQuery AJAX nostalgia**:
   ```javascript
   // The jQuery AJAX we all used
   $.ajax({
       url: '/api/users',
       method: 'GET',
       dataType: 'json',
       success: function(data) {
           console.log(data);
       },
       error: function(xhr, status, error) {
           console.error('Error:', error);
       }
   });
   ```

2. **Show the modern fetch equivalent**:
   ```javascript
   // Modern fetch API - promises everywhere!
   fetch('/api/users')
       .then(response => response.json())
       .then(data => console.log(data))
       .catch(error => console.error('Error:', error));
   ```

3. **Introduce async/await**:
   ```javascript
   // Even cleaner with async/await
   async function getUsers() {
       try {
           const response = await fetch('/api/users');
           const data = await response.json();
           console.log(data);
       } catch (error) {
           console.error('Error:', error);
       }
   }
   ```

4. **Explain the benefits**:
   - Native browser API
   - Better error handling
   - Works perfectly with modern async patterns
   - More flexible and powerful

5. **Show POST requests**:
   ```javascript
   // Posting data the modern way
   const response = await fetch('/api/users', {
       method: 'POST',
       headers: {
           'Content-Type': 'application/json',
       },
       body: JSON.stringify({ name: 'John', email: 'john@example.com' })
   });
   ```

6. **Give them a conversion exercise**: Take a jQuery AJAX call and convert it.

7. **Teach them about response.ok** and proper error handling.

8. **Challenge them** with a more complex API interaction.

9. **Celebrate**: "You're now using the same API that powers modern web frameworks!"
