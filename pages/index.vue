<template>
  <div class="content">
    <Highlight :text="highlightText" />
    <Boxes :title="title" :description="description" :boxes="boxes" />
    <Highlight :text="highlightText" />
    <Boxes :title="title" :description="description" :boxes="boxes" />
    <Boxes :title="title" :description="description" :boxes="boxes" />
  </div>
</template>

<script>

import Boxes from '~/components/sections/Boxes'
import Highlight from '~/components/sections/Highlight'

export default {
  components: {
    Boxes,
    Highlight
  },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
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
        },
        {
          title: "fourth Box",
          text: "Mauris id posuere turpis. Donec quis est ut nulla consectetur vulputate. Quisque nec elit arcu. Duis gravida massa id magna feugiat rhoncus. Morbi dapibus ac enim a luctus."
        }
      ]
    }
  }
}
</script>