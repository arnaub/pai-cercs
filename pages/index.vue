<template>
  <div class="content">
    <TextAndImage />
    <HighLightPost :highlightPost="highlightPost" v-if="highlightPost" />
    <Boxes :title="title" :description="description" :boxes="boxes" />
    <ImageAndHighlight />
    <TwoColumns :title="title" :description="description" />
  </div>
</template>

<script>

import Boxes from '~/components/sections/Boxes'
import Highlight from '~/components/sections/Highlight'
import ImageAndHighlight from '~/components/sections/ImageAndHighlight.vue'
import TextAndImage from '~/components/sections/TextAndImage.vue'
import TwoColumns from '~/components/sections/TwoColumns'
import HighLightPost from '~/components/posts/HighLightPost'

export default {
  components: {
    Boxes,
    Highlight,
    TwoColumns,
    TextAndImage,
    ImageAndHighlight,
    HighLightPost
  },
  computed: {
    highlightPost() {
      return this.$store.state.blogPosts[0];
    }
  },
  data() {
    return {
      highlightText: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus tempor, tortor eget ultricies lobortis, quam mi fermentum diam, feugiat dapibus erat ante et nulla. Quisque eu lacinia ligula.",
      title: "TITLE",
      description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus tempor, tortor eget ultricies lobortis, quam mi fermentum diam, feugiat dapibus erat ante et nulla. Quisque eu lacinia ligula. Proin tincidunt congue mauris, sit amet eleifend nisl egestas sit amet. Praesent rutrum quam in augue porttitor, malesuada aliquet enim lacinia.",
      boxes: [
        {
          title: "first Box",
          text: "Mauris id posuere turpis. Donec quis est ut nulla consectetur vulputate. Quisque nec elit arcu. Duis gravida massa id magna feugiat rhoncus. Morbi dapibus ac enim a luctus."
        },
        {
          title: "second Box",
          text: "Mauris id posuere turpis. Donec quis est ut nulla consectetur vulputate. Quisque nec elit arcu. Duis gravida massa id magna feugiat rhoncus. Morbi dapibus ac enim a luctus."
        },
        {
          title: "third Box",
          text: "Mauris id posuere turpis. Donec quis est ut nulla consectetur vulputate. Quisque nec elit arcu. Duis gravida massa id magna feugiat rhoncus. Morbi dapibus ac enim a luctus."
        }
      ]
    }
  }
}
</script>