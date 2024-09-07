<script>
    let current_status = "login";
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->

{#if current_status == "login"}
    <div>
        <h3>This is Login page</h3>
        <input type="text" name="" id="" placeholder="Enter Username" />
        <input type="password" name="" id="" placeholder="Enter Password" />
        <button>Submit</button>
        <span on:click={() => (current_status = "create")}
            >create an account!</span
        >
    </div>
{:else if current_status == "create"}
    <div>
        <h3>This is account create page</h3>

        <input type="text" name="" id="" placeholder="Enter Username" />
        <input type="password" name="" id="" placeholder="Enter Password" />
        <input type="password" name="" id="" placeholder="Re-Enter Password" />
        <button>Create</button>
        <span on:click={() => (current_status = "login")}
            >already have an account!</span
        >
    </div>
{/if}

<style lang="scss">
    div {
        display: flex;
        flex-direction: column;
        width: 20vw;
        margin: 10px;
        border: 1px solid black;
        border-radius: 10px;

        background-color: lightcyan;
        * {
            margin: 5px;
            padding: 5px;
            font-weight: bold;

        }
        button {
            width: 25%;
            background-color: wheat;
            border-radius: 5px;
            font-size: 16px;
            border:1px solid black;
            cursor: pointer;

            &:active {
                background-color: whitesmoke;
            }

        }
        span {
            background-color: lightcoral;
            text-decoration: underline;
            border-radius: 5px;
        }
    }
</style>
