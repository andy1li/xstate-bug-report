<script lang="ts">
  import { createMachine, assign } from '@xstate/fsm'
  import { useMachine } from '@xstate/svelte/lib/fsm'

  const machine = createMachine({
    id: 'machine',
    initial: 'initial',
    states: {
      initial: {},
    },
  })

  const { state, send } = useMachine(machine)
  
  console.log($state.value)
  console.log(send)
</script>

<div>
  Please check the error message in the console.
</div>