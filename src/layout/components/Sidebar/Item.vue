<style scoped>
.menu-text-wrapper {
  margin: 0 15px 0 5px;
}
</style>

<script>
export default {
  name: 'MenuItem',
  functional: true,
  props: {
    icon: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    }
  },
  render(h, context) {
    const { icon, title } = context.props
    const vnodes = []

    if (icon) {
      vnodes.push(<svg-icon icon-class={icon}/>)
    }

    if (title) {
      vnodes.push(<span slot='title' class='menu-text-wrapper'>{(title)}</span>)
    }
    return vnodes
  }
}
</script>
