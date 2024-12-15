<template>
  <li>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcStIpoB0Q4z3onxYzuzx5ugSVMOBwLVQ2EL0A&s" alt="">
    <hr>
    <slot></slot>
  </li>
</template>

<script>
export default {
  name: "MyCard"
};
</script>

<style>
li {
  background: rgba(55, 109, 225, 0.5);
    border-radius: 25px;
    width: 250px;
    text-align: center;
    padding: 10px;
    margin-bottom: 20px;
}
img {
    width: 100px;
}
</style>
