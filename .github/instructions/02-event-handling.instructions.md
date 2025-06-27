---
applyTo: 02-event-handling/**
---

# ⚡ Event Handling Evolution

When the user types "start the training":

1. **Start with jQuery nostalgia**:
   ```javascript
   // The jQuery way - so simple back then!
   $('.button').click(function() {
       alert('Clicked!');
   });
   
   $('.form').on('submit', function(e) {
       e.preventDefault();
       // handle form
   });
   ```

2. **Show the modern approach**:
   ```javascript
   // Modern event handling - more powerful!
   document.querySelectorAll('.button').forEach(button => {
       button.addEventListener('click', () => {
           alert('Clicked!');
       });
   });
   
   document.querySelector('.form').addEventListener('submit', (e) => {
       e.preventDefault();
       // handle form
   });
   ```

3. **Explain the advantages**:
   - More control over event phases
   - Better performance
   - Can remove specific listeners
   - Works with modern async patterns

4. **Teach event delegation** without jQuery:
   ```javascript
   // Event delegation the modern way
   document.addEventListener('click', (e) => {
       if (e.target.matches('.dynamic-button')) {
           // handle click
       }
   });
   ```

5. **Give them a practice exercise**: Convert a jQuery event handler to modern JavaScript.

6. **Show them `once` option** and other modern addEventListener features.

7. **Challenge them** with a more complex example involving multiple event types.

8. **Encourage them** - "See how explicit and powerful this is compared to jQuery's magic?"
