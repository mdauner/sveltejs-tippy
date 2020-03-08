<script>
  import tippy from './index';
  import { followCursor } from 'tippy.js';

  const props = {
    content: '<div class="tooltip">Styled tooltip text</div>',
    allowHTML: true,
    followCursor: true,
    plugins: [followCursor],
    onShow: function(instance) {
      console.log(instance);
    },
  };
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
  <span use:tippy={props}>Hover Me</span>
</div>
