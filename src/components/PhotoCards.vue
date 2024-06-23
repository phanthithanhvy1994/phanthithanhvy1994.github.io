<template>
  <div class="container photo-cards">
    <h2>Photo Cards:</h2>
    <div class="photo-cards-list">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <div class="image-container">
          <img :src="card.image" alt="Photo" />
        </div>
        <p>{{ card.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import photo from "../assets/photo.png";
import photo2 from "../assets/photo2.jpeg";
export default {
  name: "PhotoCards",
  data() {
    return {
      cards: [
        { image: photo2, text: "Product name is quite long in some cases." },
        {
          image: photo,
          text: "Product name is quite long in some cases. Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo2,
          text: "Product name is quite long in some cases.",
        },
        {
          image: photo,
          text: "Product name is quite long in some cases.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.photo-cards {
  margin-top: 80px;

  &-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 30px;

    .card {
      background: #fff;
      border-radius: 3px;
      box-shadow: 0 1px 4px rgba(0, 0, 0, 0.1);
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: transform 0.3s, box-shadow 0.3s;
      overflow: hidden;

      &:hover {
        transform: translateY(-10px);
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
      }

      .image-container {
        width: 100%;
        padding-top: 66.66%;
        position: relative;
        overflow: hidden;
        display: block;

        img {
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          object-fit: cover;
          border-radius: 3px;
        }
      }

      p {
        width: 100%;
        margin-top: 10px;
        padding: 10px;
        box-sizing: border-box;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
        font-weight: bold;
      }
    }
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  .photo-cards {
    margin-top: 180px;
  }
}
</style>
