<script>
  import tippy from './index';
  import { followCursor } from 'tippy.js';

  const props = {
    content: '<div class="tooltip">Styled tooltip text</div>',
    followCursor: true,
    onShow: function(instance) {
      console.log(instance);
    },
  };

  const plugins = [followCursor];
</script>

<style>
  .wrapper {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  span {
    padding: 16px;
    border-radius: 5px;
    background-color: blue;
    color: white;
    cursor: pointer;
  }

  :global(.tooltip) {
    color: orange;
    font-weight: bold;
    text-transform: uppercase;
  }
</style>

<div class="wrapper">
  <span use:tippy={{ props, plugins }}>Hover Me</span>
</div>
