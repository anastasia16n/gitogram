<template>
  <div class="topline">
    <topline>
      <template #headline>
        <div class="icon">
          <icon name="home" />
        </div>
      </template>
      <template #content>
        <ul class="stories">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item
              :avatar="story.avatar"
              :username="story.username"
              @onPress="handlePress(story.id)"
            />
          </li>
        </ul>
      </template>
    </topline>
  </div>
</template>

<script>
import { topline } from '../../components/topline'
import { stories } from './data.json'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Feeds',
  components: {
    topline
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" scoped>
  .icon {
    width: 32px;
    height: 32px;
  }
</style>
