<template>
    <div class="flex">
        <form action="#">
            <h1>LOGIN</h1>
            <p>USERNAME</p>
            <input type="text" class="username" placeholder="input username" required>
            <p>PASSWORD</p>
            <input :type='inputpass' class="pass" placeholder="input password" required minlength="6"><span class="tombol" v-on:click="tombol"><i class="far fa-eye"></i></span><br>
            <button class="submit"><b>SUBMIT</b></button>
        </form>
    </div>
</template>

<script>
export default {
  name: 'LoginForm',
  data(){
      return{
          inputpass: 'password'
      }
  },
  methods: {
      tombol(){
        if(this.inputpass == 'password'){
            this.inputpass = 'text'
        }else{
            this.inputpass = 'password'
        }
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
        html, body{
            margin: 0;
            height: 100%;
            /* background-color: blue; */
            background-image: url('https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.123freevectors.com%2Fwhite-and-gold-background-vector-image-157866%2F&psig=AOvVaw0Dn_aAizwXgzt7003v5n4B&ust=1633874309115000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCPits6m-vfMCFQAAAAAdAAAAABAD');
            background-size: cover;
        }

        .flex {
            display: flex;
            width: 100%;
            height: 100%;
            justify-content: center;
            align-items: center;
        }

        form {
            box-sizing: border-box;
            text-align: center;
            padding-bottom: 30px;
            width: 500px;
            height: 415px;
            background-color: white;
            box-shadow: 5px 10px 8px #888888;
        }

        h1 {
            margin-top: 40px;
            letter-spacing: 2px;
            color: rgb(230, 184, 73);
            margin-bottom: 40px;
        }

        p {
            margin-bottom: 5px;
            font-size: 20px;
            letter-spacing: 2px;
            color: rgb(230, 184, 73);
        }

        .username {
            margin-top: 2px;
            width: 300px;
            height: 20px;
        }

        .pass {
            margin-top: 2px;
            width: 265px;
            height: 20px;
        }

        .tombol {
            box-sizing: border-box;
            border-radius: 5px;
            margin-left: 2px;
            background-color: rgb(230, 184, 73);
            padding: 3px 6px 3px 6px;
        }

        .tombol,.submit:hover {
            cursor: pointer;
        }

        .tombol:active {
            background-color: rgb(201, 162, 72);
        }

        .submit {
            margin-top: 30px;
            font-family: "Baloo 2";
            color: rgb(255,255,255);
            font-size: 20px;
            width: 200px;
            height: 40px;
            background-color: rgb(230, 184, 73);
            border-color: rgb(230, 184, 73);
        }

        .submit:active {
            color: rgb(255,255,255);
            background-color: rgb(199, 158, 73);
            border-color: rgb(199, 158, 63);
        }
</style>
