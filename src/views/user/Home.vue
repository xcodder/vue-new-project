<template>
  <div class="user-grid-1">
    <header>
      <div class="header-container">
        <h1 class='logo'>
          toofel
        </h1>
        <ul class='header-links'>
          <li v-for='link in ["Home", "My Contacts"]'>
            <a href="#">
              {{link}}
            </a>
          </li>
        </ul>
      </div>
    </header>
    <main class='user-grid-2'>
      <div class="left-bar">
        <ul class="contact-groups">
          <li v-for='name in ["Contacts", "pwds.io", "fxp", "pro"]'>
            <span>
              {{name}}
            </span>
          </li>
        </ul>
      </div>
      <section class='right'>
        <div class="group-info">
          <h3 class='group-title'>Contacts</h3>
          <p class='group-desc'>My main group for my general contacts.</p>
        </div>
        <div class="flex">

          <ul class='chats'>
            <li v-for='chat in chats'>
              <Msg :title='chat.title' :content='chat.content' />
            </li>
          </ul>
          <section class='main-conv'>
            <Msg :title='mainConv.title' :content='mainConv.content' />
            <div class="send-message-box">
              <textarea class='post-message'></textarea>
              <div class="send-message-btn-container">
                <button type="button" class='send-message'>Send</button>
              </div>
            </div>
          </section>

        </div>
      </section>
    </main>
    <!-- <input type="text" class="search-input" placeholder="Find..."> -->
  </div>
</template>

<script>
import Msg from '@/components/Msg'
export default {
  name: 'UserHome',
  components: {
    Msg
  },
  data() {
    return {
      mainConv: {
        title: "Hello Jerry",
        content: `I wanted to tell about a new report we've found while searching for methods to help us spare our resources in order to optimize our energy and money consumtion with amazon aws.

As you can see in the following links, based on a study which had been taken place, the conclusions which are to be taken into account are that a place with high atmosity in the air shall not benefit our ecological system.

  https://searchnet.com/ecological-damage-in-web-area
  https://searchnet.com/why-you-should-not-host-your-server-near-waterfull-area

Yours,
Jason Beckard`
      },
      chats: [
        {
          title: "Hello Jerry",
          content: "I wanted to tell about a new report we've found while searching..."
        },
        {
          title: "What's up",
          content: "It's alem from stips"
        },
        {
          title: "Good game",
          content: "I was juventus 5-3 against you. Played well"
        }
      ]
    }
  }
}
</script>

<style scoped>
.search-input {
  padding: 5px 6px;
  border: 1px solid gainsboro;
  border-radius: 2px;
  font-size: 19px;
}
.user-grid-1 {
  display: flex;
  flex-direction: column;
}
.user-grid-2 {
  display: flex;
}
.contact-groups {
  display: flex;
  flex-direction: column;
}
.contact-groups > li {
  padding: 7px 16px;
  border-bottom: 1px solid #e2e2e2;
  min-width: 152px;
}
.contact-groups > li > span {
  font-size: 19px;
  color: #464343;
}
header {
  background: #a92c2c;
  margin-bottom: 15px;
}
.chats {

}
.chats > li {

}

.left-bar {
  border-right: 1px solid gainsboro;
  margin-right: 10px;
}
.header-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 9px 0;
  display: flex;
  align-items: center;
}
.header-container .logo {
  color: #f9f9f9;
  font-size: 20px;
  letter-spacing: 2px;
}
.flex {
  display: flex;
}
.right {
  display: flex;
  flex-direction: column;
}
.group-info {
  margin-bottom: 20px;
  padding: 7px 6px;
  border: 1px solid gainsboro;
  border-radius: 3px;
  display: flex;
  align-items: center;
}
.group-title {
  font-size: 20px;
  margin-right: 12px;
}
.group-desc {
  color: gray;
}
.main-conv {
  margin-left: 6px;
  max-width: 641px;
  display: flex;
  flex-direction: column;
}
.send-message-box {
  display: flex;
  flex-direction: column;
}
.post-message {
  border: 1px solid gainsboro;
  resize: none;
  height: 82px;
  padding: 9px 9px;
}
.send-message {
  margin-top: 3px;
  padding: 5px 9px;
  border: 1px solid #c1c1c1;
  color: #4c4c4c;
  background: #fffefe;
  border-radius: 3px;
}
.send-message-btn-container {
  display: flex;
  justify-content: flex-end;
}
.header-links {
  display: flex;
  margin-left: 20px;
}
.header-links > li {
  margin-right: 20px;
}
.header-links > li > a {
  color: white;
}
</style>
