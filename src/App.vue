<template>
  <main>
    <div class="icons">
      <iconLove class="icon-large icon-pink" />
      <iconDeath class="icon-large icon-black" />
      <iconRobot class="icon-large icon-green" />
    </div>
    <div class="text">
      <h1>
        <span class="pink">Inline </span> <span class="black">SVG </span>
        <span class="green"> Icons</span>
      </h1>
      <p>Zero HTML Requests + CSS customization</p>
    </div>

    <div class="buttons">
      <a
        href="https://medium.com/@dmitrymind/inline-svg-icons-in-vuejs-6b3e3f488912"
      >
        Read on Medium
      </a>
      <a href="https://github.com/artrayd/SVG-Icon-Font"
        >Download from GitHub</a
      >
    </div>
  </main>
</template>
<script>
import iconLove from "./components/icon/Love.vue";
import iconDeath from "./components/icon/Death.vue";
import iconRobot from "./components/icon/Robot.vue";

export default {
  name: "App",
  components: {
    iconLove,
    iconDeath,
    iconRobot,
  },
};
</script>

<style lang="scss">
$pink: #ff43a8;
$black: #333333;
$green: #00c95c;

body,
html {
  width: 100%;
  height: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

main {
  margin-bottom: 40px;
  .icons {
    svg {
      margin: 12px;
    }
    .icon-love path {
      fill: $pink;
    }

    .icon-death path {
      fill: $pink;
    }

    .icon-robot path {
      fill: #00c95c;
    }
  }

  .text {
    h1 {
      font-size: 40px;
      letter-spacing: 0.5px;
      margin-bottom: 0;
    }

    p {
      letter-spacing: 1px;
    }
  }

  .buttons {
    margin-top: 40px;
    display: flex;
    a {
      padding: 8px 16px;
      color: $black;
      text-decoration: none;
      border: 1px solid $black;
      border-radius: 24px;
      margin: 0 8px;

      &:hover {
        text-decoration: underline;
      }
    }
  }
}

.icon-pink path {
  fill: $pink;
}

.icon-black path {
  fill: $black;
}

.icon-green path {
  fill: $green;
}

.pink {
  color: $pink;
}

.black {
  color: $black;
}

.green {
  color: $green;
}

.icon-large {
  width: 48px;
  height: 48px;
}
.icon-default {
  width: 24px;
  height: 24px;
}

.icon-small {
  width: 16px;
  height: 16px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
