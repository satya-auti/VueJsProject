<template>
    <div>
        <form method="post" action="">
        <table  class="center"  >
            <caption style="color: red; font-weight: bold; ">
                
                <!-- Employee Registration Form -->
                <div>
                    <h2><img src="./images/img_100.jpg" height="70px" width="70px"> Employee Registration Form</h2> 
                </div>
            </caption>
            <tr>
                <td></td>
                <td>
                    <!-- salutation -->
                    <div>
                        <input type="radio" name="salutation" id="Mr" value="Mr" checked    >
                        <label for="Mr">Mr.</label>

                        <input type="radio" name="salutation" id="Mrs" value="Mrs">
                        <label for="Mrs">Mrs.</label>

                        <input type="radio" name="salutation" id="Ms" value="Ms">
                        <label for="Ms">Ms.</label>
                    </div>
                </td>
            </tr>
            <!-- First Name -->
            <tr>
                <td>
                    <label for="firstName">First Name</label>
                </td>
                <td>
                    <input type="text" name="firstName" id="firstName" placeholder="First Name" required>
                </td>
            </tr>

            <!-- Last Name -->
            <tr>
                <td>
                    <label for="lastName">Last Name</label>
                </td>
                <td>
                    <input type="text" name="lastName" id="lastName" placeholder="Last Name" required>
                </td>
            </tr>

            <!-- Mail Address1 -->
            <tr>
                <td>
                    <label for="mailAddress1"> Mail Address1</label>
                </td>
                <td>
                    <input type="text" name="mailAddress1" id="mailAddress1" placeholder=" " required>
                </td>
            </tr>

            <!-- Mail Address2 -->
            <tr>
                <td>
                    <label for="mailAddress2">Mail Address2 </label>
                </td>
                <td>
                    <input type="text" name="mailAddress2" id="mailAddress2" placeholder=" "required>
                </td>
            </tr>
            
            <!-- City -->
            <tr>
                <td>
                    <label for="city">City</label>
                </td>
                <td>
                    <input type="text" name="city" id="city" placeholder=" " required>
                </td>
            </tr>

            <!-- State -->
            <tr>
                <td>
                    <label for="state">State</label>
                </td>
                <td>
                    <select  id="state" required>
                        <option    value="Gujarat">Gujarat </option>
                        <option    value="Maharashtra">Maharashtra </option>
                        <option    value="Rajasthan">Rajasthan </option>
                        <option    value="Kerala">Kerala </option>
                        <option    value="Punjab">Punjab </option>
                        <option    value="Jammu Kashmir">Jammu Kashmir </option>
                    </select>
                </td>
            </tr>

            <!-- Zip -->
            <tr>
                <td>
                    <label for="zip">Zip</label>
                </td>
                <td>
                    <input type="text" name="zip" id="zip" placeholder=" " required>
                </td>
            </tr>

            <!-- Photo -->
            <tr>
                <td>
                    <label for="photo">Upload Photo</label>
                </td>
                <td>
                    <input type="file" name="photo" id="photo" onchange="return fileValidation()" placeholder=" ">
                    <!-- Image preview -->
	                <div class="flex" id="imagePreview" ></div>
                </td>
                
            </tr>

            <!-- Email -->
            <tr>
                <td>
                    <label for="email">Email </label>
                </td>
                <td>
                    <input type="email" name="email" id="email" placeholder="" required> 
                </td>
            </tr>

            <!-- Mobile -->
            <tr>
                <td>
                    <label for="mobile"> Mobile</label>
                </td>
                <td>
                    <input type="text" name="mobile" id="mobile" placeholder="+91 " required>
                </td>
            </tr>

            <!-- Language -->
            <tr>
                <td style="vertical-align:top">
                    <label for="lang">Language Known  </label>
                </td>
                <td>
                    <input type="checkbox" name="lang" id="Gujarati" value="Gujarati" checked >
                    <label for="Gujarati">Gujarati</label> <br>

                    <input type="checkbox" name="lang" id="Hindi" value="Hindi" checked >
                    <label for="Hindi">Hindi</label><br>

                    <input type="checkbox" name="lang" id="English" value="English" checked>
                    <label for="English">English</label><br>

                    <input type="checkbox" name="lang" id="Marathi" value="Marathi" >
                    <label for="Marathi">Marathi</label>
                    
                </td>
            </tr>

            <!-- Addition Info -->
            <tr>
                <td>
                    <label for="info"> Addition Information</label>
                </td>
                <td>
                    <textarea name="info" id="info" placeholder="Optional" rows="4"></textarea>
                </td>
            </tr>
            <!-- Password -->
            <tr>
                <td>
                    <label for="password"> Password </label>
                </td>
                <td>
                    <input type="password" name="password" id="password" placeholder="Password" onchange="verifyPassword()" >
                    <p id="errorPassword"></p>
                </td>
            </tr>

            <!-- Submit Reset Buttons -->
            <tr>
                <td>
                    <input type="button" name="check" onclick="validations()" value="Check">
                </td>
                <td>
                    <input type="submit" name="submit"  onclick="userDetails()" value="Submit">
                    <input type="reset" name="reset" value="Reset">
                </td>
            </tr>
        </table>
    </form>
    </div>
</template>

<script>
 export default {
    name: 'App',
    data(){
            return {
            
            };
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