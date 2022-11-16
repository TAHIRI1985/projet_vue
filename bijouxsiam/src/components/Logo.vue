<template>
     <div class="col">
        <a href="#">
            <img :src="require(`@/assets/${image}`)" width="50" height="50"><br>
                 
                  {{titre}}
        </a>
     </div>
</template>
<script>
export default {
  name: 'Logos',
  props: {
    id: Number,
    titre:String,
    image:String,
  }
}
</script>