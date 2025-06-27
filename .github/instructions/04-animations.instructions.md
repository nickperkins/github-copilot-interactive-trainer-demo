---
applyTo: 04-animations/**
---

# ✨ Animation Revolution

When the user types "start the training":

1. **Remember jQuery animations**:
   ```javascript
   // jQuery animations - remember this?
   $('.box').fadeIn();
   $('.modal').slideDown(300);
   $('.button').animate({
       left: '250px',
       opacity: 0.5
   }, 1000);
   ```

2. **Introduce CSS transitions**:
   ```css
   /* CSS transitions - smooth and performant */
   .box {
       opacity: 0;
       transition: opacity 0.3s ease-in-out;
   }
   
   .box.visible {
       opacity: 1;
   }
   ```

   ```javascript
   // JavaScript just toggles classes
   document.querySelector('.box').classList.add('visible');
   ```

3. **Show CSS animations for complex sequences**:
   ```css
   @keyframes slideIn {
       from {
           transform: translateX(-100%);
           opacity: 0;
       }
       to {
           transform: translateX(0);
           opacity: 1;
       }
   }
   
   .animate-in {
       animation: slideIn 0.5s ease-out;
   }
   ```

4. **Explain the performance benefits**:
   - GPU acceleration
   - Smoother 60fps animations
   - Less JavaScript blocking
   - Better battery life on mobile

5. **Introduce the Web Animations API** for when you need JavaScript:
   ```javascript
   // Web Animations API - the future!
   element.animate([
       { transform: 'translateX(0px)' },
       { transform: 'translateX(300px)' }
   ], {
       duration: 1000,
       easing: 'ease-in-out'
   });
   ```

6. **Give them a conversion exercise**: Turn a jQuery animation into CSS + JavaScript.

7. **Show them `requestAnimationFrame`** for custom animations.

8. **Challenge them** to create a complex animation sequence.

9. **Celebrate their modern skills**: "Your animations are now buttery smooth and battery-friendly!"
