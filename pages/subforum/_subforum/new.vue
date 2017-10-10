<template>
<section>
  <div id="title-wrapper">
    <h1>New Post</h1>
  </div>
  <form>
    <!-- Test trim -->
    <input
      v-model.trim="postTitle" 
      type="text" 
      placeholder="Post Title" 
      onfocus="this.placeholder=''" 
      onblur="this.placeholder='Post Title'"
    />
    <!-- Test trim -->
    <textarea
      v-model.trim="postContent"
      placeholder="Post Content" 
      onfocus="this.placeholder=''" 
      onblur="this.placeholder='Post Content'"
    />
    <div id="create-post-wrapper">
      <button
        v-if="postTitle !== '' && postContent !== ''"
        @click.prevent="submitPost"
        id="enabled-button"
      >
        <i class="fa fa-plus" aria-hidden="true"/>Create Post
      </button>
      <button 
        v-else
        disabled
        id="disabled-button" 
        title="Both the post title and post content sections are required" 
      >
        <i class="fa fa-plus" aria-hidden="true"/>Create Post
      </button>
    </div>
  </form>
</section>
</template>

<script>
export default {
  data() {
    return {
      postTitle: '',
      postContent: ''
    }
  },
  methods: {
    submitPost() {
      const { postTitle, postContent } = this;
      if (postTitle !== '' && postContent !== '') {
        console.log(`${postTitle}\n${postContent}`);
      }
    }
  },
  head: () => 'New Post'
}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/variables';

section {
  flex-grow: 1;
  margin: 2rem;
  display: flex;
  flex-direction: column;
  font-size: 1.5rem;
  background-color: white;
  border-radius: 0.5rem;
  box-shadow: 10px 10px 25px #999;
}

#title-wrapper {
  display: block;
  border-radius: 0.5rem 0.5rem 0 0;
  margin: 0;
  padding: 0.75rem;
  background-color: $primary-blue;
  color: white;

  h1 {
    margin: 0;
    padding: 0;
    font-size: 2.5rem;
  }
}

form {
  flex-grow: 1;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;

  input, 
  textarea {
    padding: 1.25rem;
    margin-bottom: 1rem;
    font-size: 1.65rem;
    border: none;
    border-radius: 0.5rem;
    background-color: #eee;
    font-size: 1.5rem;
    outline: none;
  }

  textarea {
    padding: 1.25rem;
    resize: none;
    border-radius: 0.5rem;
    flex-grow: 1;
  }
}

#create-post-wrapper {
  display: flex;
  flex-direction: row-reverse;

  button {
    font-size: 1.2rem;
    width: 15rem;
    padding: 1rem;
    border: none;
    border-radius: 5px;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: 600;
    outline: none;
    transition: 0.15s ease-in-out;

    i {
      margin-right: 0.5rem;
      transition: 0.15s ease-in-out;
    }
  }
}

#disabled-button {
  color: white;
  background-color: grey;
  cursor: not-allowed;

  i {
    color: white;
  }
}

#enabled-button {
  background: $primary-blue;
  color: white;

  i {
    color: $nav-hover;
  }

  &:hover {
    background-color: $nav-hover;

    i {
      color: white;
    }
  }
}

</style>