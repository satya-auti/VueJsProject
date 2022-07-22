<template>
<div>
            <pre>
                {{JSON.stringify(formValues,null,2)}}
            </pre>
        </div>
        <!--  -->
    <div class="">
        


         <form @submit="submitForm" method="post">


            <table border="2">
                <caption>User Registration</caption>
                <tr>
                    <td>
                        <label for="firstName">First Name</label>
                    </td>
                    <td>
                        <input type="text" name="firstName" v-model="formValues.firstName" id="firstName" placeholder="First Name" required/>
                    </td>
                </tr>

                <tr>
                    <td>
                        <label for="lastName">Last Name</label>
                    </td>
                    <td>
                        <input type="text" name="lastName" id="lastName" v-model="formValues.lastName" placeholder="Last Name" required/>
                    </td>
                </tr>

                <tr>
                    <td>
                        <label for="email">Email</label>
                    </td>
                    <td>
                        <input type="email" name="email" id="email" v-model="formValues.email" placeholder="Email " required/>
                    </td>
                </tr>


                 <tr>
                    <td>
                        <label for="gender">Gender</label>
                    </td>
                    <td>
                        <input type="radio" name="gender" value="Male" id="male" v-model="formValues.gender" selected/>
                        <label for="male">Male</label>

                        <input type="radio" name="gender" value="Female" id="female" v-model="formValues.gender" />
                        <label for="female">Female</label>

                        <input type="radio" name="gender" value="Other" id="other" v-model="formValues.gender" />
                        <label for="other">Other</label>
                    </td>
                </tr>


                <tr>
                    <td>
                        <label for="country">Country</label>
                    </td>
                    <td>
                        <select id="country" v-model="formValues.country">
                            <option value="">Select a Country</option>
                            <option value="india">India</option>
                            <option value="brazil">Brazil</option>
                            <option value="australia">Australia</option>
                            <option value="nepal">Nepal</option>
                            <option value="japan">Japan</option>
                            <option value="usa">USA</option>
                            <option value="germany">Germany</option>
                            <option value="srilanka">SriLanka</option>
                            <option value="vietnam">vietnam</option>
                            <option value="singapore">Singapore</option>
                        </select>
                    </td>
                </tr>

                <tr>
                    <td>

                        <input type="checkbox" name="terms" id="terms" false-value="no" true-value="yes" v-model="formValues.terms"/>
                    </td>
                    <td>
                        <label for="terms">Terms & Conditions</label>
                    </td>
                </tr>

                <tr>
                    <td>

                        
                    </td>
                    <td>
                        <input type="submit" class="rounded-lg text-white px-3 p-1 bg-lime-600 hover:bg-lime-700" name="submit" id="submit"  value="Submit"/>
                        <input type="reset" class="rounded-lg text-white px-3 p-1 bg-red-600 hover:bg-red-700" name="reset" id="reset"  value="Reset"/>
                    </td>
                </tr>
            </table>

         </form>          
            <!--  -->
       
    </div>
</template>

<script>
 export default {

        name:'App',
        data(){
            return {
                formValues: {
                    firstName: '',
                    lastName: '',
                    email: '',
                    gender: '',
                    country: '',
                    terms: "no",
                }
            };
        },
        methods: {
            submitForm(event) {
                event.preventDefault();
                console.log("Form Values", this.formValues);
            }
        },


};

  
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>