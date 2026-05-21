<template>
  <div class="profile-image">
    <img src="../../public/image/profile.jpeg" alt="Profile Image" />
  </div>
</template>

<script>
export default {
  name: "ProfileImage",
};
</script>

<style scoped>
.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  overflow: hidden;
  margin-bottom: 1rem;
  position: absolute;
  left: 100px;
}

.profile-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>