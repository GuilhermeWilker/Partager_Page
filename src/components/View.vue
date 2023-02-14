<template>
  <div class="view">
    <header>
      <nav>
        <ul>
          <li>
            <a
              href="https://www.linkedin.com/in/guilherme-wilker-3a8294189/"
              target="_blank"
              >Contato</a
            >
          </li>
          <li>Reportar erro ou bug</li>
        </ul>
      </nav>
    </header>

    <h1 class="title">Seu jeito novo de ouvir musíca!</h1>
    <p class="paragraph">
      Esqueça os players de música chatos e formais, é hora de se divertir com
      nosso player de música incrível!!
    </p>

    <Button content="Começar agora!" class="btn" />
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "View",
  components: {
    Button,
  },
};
</script>

<style scoped>
.view {
  width: 500px;
}

header {
  width: 100%;
}
ul {
  list-style-type: none;
  font-size: 14px;
}

nav ul {
  display: flex;
  gap: 50%;

  margin-left: -50px;

  align-items: center;
}

nav ul li {
  cursor: pointer;
}

nav ul li a {
  text-decoration: none;
}

nav ul li:last-child {
  color: white;
  border-radius: 5px;
  background: #2778f2;
  padding: 12px;

  cursor: pointer;
  transition: 0.2s all;
}

nav ul li:last-child:hover {
  background: #2778f2;
}

.title {
  width: 442px;

  font-weight: 700;
  font-size: 48px;

  margin: 220px 0 20px 0;
}

.paragraph {
  font-size: 16px;
  width: 400px;

  margin-bottom: 40px;
}

@media (max-width: 430px) {
  .view {
    width: 100%;
  }

  header {
    width: 430px;
  }
  .title {
    text-align: center;
    margin: 100px 0 20px 0;

    width: 100%;
  }

  .paragraph {
    text-align: center;
    width: 100%;
  }

  .btn {
    margin: 0 30%;
  }

  nav ul {
    margin: 0 0.5px;
    font-size: 13px;

    align-items: center;
  }
}
</style>
