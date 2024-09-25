<script lang="ts">
    export let id: string;
    export let type: string;
    export let label: string;
    export let autocomplete: string | undefined = undefined;
    export let required: boolean = false;
</script>

<div class="Field">
    <label for={id}>
        {label}
    </label>
    <input name={id} {id} {type} {autocomplete} {required} />
</div>