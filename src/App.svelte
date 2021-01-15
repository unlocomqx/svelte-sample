<script>
  let count = 0;

  $: double = count * 2;
  $: quadruple = count * 4;
  setInterval(() => {
    count++;
  }, 5000);

  setTimeout(() => {
    count++;
  }, 1000);

  let counter = 0;
  let double_counter = 0;
  $: {
    double_counter = counter * 2;
  }

</script>

<p>
  {count} * 2 = {double}
</p>

<p>
  {count} * 4 = {quadruple}
</p>

<button on:click={() => counter++}>
  Add
</button>

Result: {double_counter}
