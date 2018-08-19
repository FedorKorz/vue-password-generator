<template>
    <div>
        <h2>Password generator</h2>
        <div class="wrapper">
            <span @click="select()">
                <input id="password-box" v-bind:value="password">
            </span>
            <span class="password-length">
                {{ passwordLenght }} 
            </span>
            <span class='update-password' v-on:click='updatePassword'></span>
            <span class='copy-password' v-on:click='copyPassword'></span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'PasswordBox',
        props: ['password', 'passwordLenght'],
        methods: {
  	        select() {
    	        this.$emit('selected');
            },
            copyPassword() {
                var copyText = document.getElementById("password-box");
                copyText.select();
			    document.execCommand("copy");
            },
            updatePassword() {
                this.$emit('generatePass');    
            }
        }
    };
</script>

<style>
    h2 {
        font-family: 'Righteous', cursive;
        margin: 0;
        padding-top: 50px;  
    }

    .password-length {
        font-family: 'Righteous', cursive;    
    }
    
    .update-password {
        margin-top: 12px;
        width: 20px;
        height: 20px;
        background-repeat: no-repeat;
        background-image: url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMjIgM3YxOGgtNXYtMmgzdi0xNGgtNnYzbC01LjI1LTQgNS4yNS00djNoOHptLTEyIDE2aC02di0xNGgzdi0yaC01djE4aDh2M2w1LjI1LTQtNS4yNS00djN6Ii8+PC9zdmc+");
    }

    .copy-password {
        margin-top: 12px;
        width: 20px;
        height: 20px;
        background-repeat: no-repeat;
        background-image: url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTggNnYtNmgtMTh2MThoNnY2aDE4di0xOGgtNnptLTEyIDEwaC00di0xNGgxNHY0aC0xMHYxMHptMTYgNmgtMTR2LTE0aDE0djE0em0tMy04aC0zdi0zaC0ydjNoLTN2MmgzdjNoMnYtM2gzdi0yeiIvPjwvc3ZnPg==");   
    }

    .wrapper {
        display: flex;
        justify-content: center;
    }

    .wrapper span {
        padding: 10px;
    }

    #password-box {
        width: 230px;
        height: 30px;
        border: none;
        border-radius: 5px;
        font-family: 'Righteous', cursive;
        padding-left: 10px;
    }

    .password-length {
        width: 10px;
        margin: 5px;
        margin-left: -5px;
    }
</style>

