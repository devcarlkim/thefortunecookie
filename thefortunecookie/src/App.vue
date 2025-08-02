<script setup></script>

<template>
  <h1>The Fortune Cookie. 🍪</h1>
  </br>
  <p></p>
  <h2>Your Fortune:</h2>
  <h3>{{ displayCurrentFortune }}</h3>
  <button @click="generateFortune">See your fortune!</button>
</template>
<script> 
export default {
  data() {
    return {
        currentFortuneText: 'Click on the button to see your fortune.',
        currentFortuneIndex: 0,
        fortunesList: [
          "🌟 You will find happiness in unexpected places.",
          "🎉 A thrilling time is in your near future.",
          "🧪 Now is the time to try something new.",
          "🔍 You will make a valuable discovery today.",
          "🎁 A pleasant surprise is waiting for you.",
          "🚀 Success will come when you least expect it.",
          "👑 You are destined for greatness.",
          "🌈 The best is yet to come.",
          "🏆 Your talents will be recognized and rewarded.",
          "🔓 A new opportunity will present itself soon.",
          "🛤️ You will soon embark on a journey of growth.",
          "🕰️ Stay patient; your hard work will pay off.",
          "💖 You will be surrounded by love and laughter.",
          "🧭 Trust your instincts—they’re leading you well.",
          "✨ You will inspire someone today.",
          "🤝 A small act of kindness will bring you joy.",
          "🔮 The answer you seek is already within you.",
          "🦁 Your courage will guide you through challenges.",
          "💡 Believe in yourself and all that you are.",
          "☀️ Your future is as bright as your faith.",
          "🌠 A dream you have will come true soon.",
          "💪 You are stronger than you think.",
          "🕊️ A peaceful moment is coming your way.",
          "📈 Growth is in your path—embrace it.",
          "🧘 Clarity will come when you slow down.",
          "🎯 Your goals are within reach.",
          "📬 Good news will arrive unexpectedly.",
          "🌼 Smile—you’re making someone’s day better.",
          "💫 Magic happens when you don’t give up.",
          "🛡️ Stay true to your values—they’ll protect you.",
          "🍀 Luck is on your side today.",
          "📚 You will learn something valuable very soon.",
          "🖼️ A new perspective will change everything.",
          "🎨 Creativity will lead you to joy.",
          "🎵 A beautiful moment is waiting in silence.",
          "🧠 Sharpen your mind; it will guide you well.",
          "🌙 Take time to rest—answers will follow.",
          "🌳 Patience will bring long-term rewards.",
          "🌊 Go with the flow; resistance creates stress.",
          "🛎️ An unexpected visitor will bring good vibes.",
          "🌻 Let your light shine unapologetically.",
          "🔥 Passion will fuel your next big step.",
          "🍰 Celebrate even the smallest wins.",
          "📦 Think outside the box—it’s worth it.",
          "🛠️ Build your dreams one brick at a time.",
          "💌 A heartfelt message is coming your way.",
          "🎈 Joy is found in the little things.",
          "📅 Tomorrow holds a beautiful surprise.",
          "🪞 Self-reflection will unlock clarity.",
          "🪄 What feels ordinary may become extraordinary.",
          "🧩 The missing piece will soon appear.",
          "🧤 You are protected in more ways than you know."
        ],
    }
  },
  computed: {
    //@Todo
    displayCurrentFortune() {
      return this.currentFortuneText;
    }
  },
  methods: {
    generateFortune() {
      const randomIndex = Math.floor(Math.random() * 10) + 1;
      while (randomIndex == this.currentFortuneIndex) {
        randomIndex = Math.floor(Math.random() * 49) + 1;
      }

      this.currentFortuneText = this.fortunesList[randomIndex];
      return 0
    }
  }
}
</script>

<style scoped></style>
