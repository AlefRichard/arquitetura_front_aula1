<template>
    <header>
      <div class="container">
        <nav>
          <ul>
            <li><nuxt-link to="#">Blog</nuxt-link></li>
            <li><nuxt-link to="#">Sobre</nuxt-link></li>
            <li><nuxt-link to="#">Descrição</nuxt-link></li>
          </ul>
        </nav>
      </div>
    </header>

  <main class="about-content">
    <div class="container">
      <div class="profile">
        <div class="profile-info">
          <div class="profile-image">
            <img src="/public/octo.png" alt="Foto do Alef" />
          </div>
          <div class="profile-details">
            <h1>Alef Richard</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam ultrices, metus in auctor suscipit, arcu sem consectetur arcu, sit amet eleifend mauris magna et orci. Aenean rhoncus congue sapien, in convallis tortor sollicitudin quis. Nulla mi dui, fermentum eget suscipit vitae, tempor sagittis sapien. In pretium dignissim viverra. Cras vulputate fermentum odio, vitae egestas turpis semper vitae. Curabitur scelerisque, risus in commodo convallis, mauris leo feugiat elit, vitae semper risus purus in mauris. Pellentesque id ipsum sed risus vehicula semper. In hac habitasse platea dictumst. Proin ut dolor quis nulla tempor condimentum.</p>
          </div>
        </div>
      </div>
    </div>
  </main>

  <div class="blog-section">
    <h2>Últimas postagens do blog</h2>
    <div class="blog-posts">
      <div class="blog-post" v-for="post in posts" :key="post.id">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt }}</p>
      </div>
    </div>
  </div>
    
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: 'Post 1', excerpt: 'Nullam non libero ut purus finibus lacinia. Nam blandit dictum mi, a finibus leo dapibus sit amet. Integer eget sem justo. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus...' },
        { id: 2, title: 'Post 2', excerpt: 'Nullam non libero ut purus finibus lacinia. Nam blandit dictum mi, a finibus leo dapibus sit amet. Integer eget sem justo. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus...' },
        { id: 3, title: 'Post 3', excerpt: 'Nullam non libero ut purus finibus lacinia. Nam blandit dictum mi, a finibus leo dapibus sit amet. Integer eget sem justo. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus...' },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "@/assets/css/main.css";
</style>