---
title: "Contact"
layout: single
permalink: /contact/
---

<form action="https://formspree.io/f/xleyqlwj" method="POST">
    <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" required maxlength="50" placeholder="Your Name">
    </div>
    <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" name="_replyto" required maxlength="100" placeholder="your.email@example.com">
    </div>
    <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" name="message" rows="3" required maxlength="500" placeholder="Your message"></textarea>
        <div id="message-count" style="text-align: right; color: #555;">0/500</div>
    </div>
    <div style="margin-top: -10px;">
        <button type="submit">Send</button>
    </div>
</form>

<script>
  var messageInput = document.getElementById('message');
  var messageCountElement = document.getElementById('message-count');
  var maxMessageLength = messageInput.maxLength;

  messageInput.addEventListener('input', function() {
    var messageLength = this.value.length;
    messageCountElement.textContent = messageLength + '/' + maxMessageLength;

    // Change color to red if the user is within 10% of the limit
    if (messageLength > maxMessageLength * 0.9) {
      messageCountElement.style.color = 'red';
    } else {
      messageCountElement.style.color = '#555'; // Default color
    }
  });
</script>
