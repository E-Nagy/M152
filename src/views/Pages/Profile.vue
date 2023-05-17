<template>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  
    <dialog open>
      <form action="?" method="dialog">
        <div class="section">
          <div class="form-elements">
            <label for="username">Username</label>
            <input type="text" name="username" />
          </div>
          <div class="form-elements">
            <label for="vorname">Vorname</label>
            <input type="text" name="vorname" />
            <label for="nachname">Nachname</label>
            <input type="text" name="nachname" />
          </div>
        </div>
        <div class="section">
          <div class="form-elements">
            <label for="strasse">Strasse</label>
            <input type="text" name="strasse" />
          </div>
          <div class="form-elements">
            <label for="plz">PLZ</label>
            <input type="text" name="plz" />
            <label for="ort">Ort</label>
            <input type="text" name="ort" />
          </div>
        </div>
        <div class="section">
          <div class="form-elements">
            <label for="lehrjahr">Lehrjahr</label>
            <input type="text" name="lehrjahr" />
          </div>
        </div>
        <div class="form-elements">
          <label for="email">E-Mail</label>
          <input type="email" name="email" />
        </div>
        <div class="form-elements">
          <label for="pwd">Passwort</label>
          <input type="text" name="pwd" />
        </div>
        <div class="form-elements">
          <button type="submit">Submit</button>
        </div>
      </form>
    </dialog>
  </template>
  <style lang="scss">
  .section {
    margin-bottom: 20px;
  }
  .form-elements {
    display: flex;
    label,
    input {
      margin-bottom: 20px;
    }
    label {
      padding-right: 10px;
      padding-left: 10px;
      font-weight: bold;
      width: 70px;
      align-self: flex-end;
    }
    input {
      width: auto;
      margin-right: 30px;
      border-radius: 5px;
      padding: 5px 10px;
    }
  }
  button {
    margin-left: 90px;
    height: 30px;
    width: 185px;
    border-radius: 5px;
    padding: 5px 10px;
  }
  dialog {
    z-index: 10;
    margin-top: 10px;
    background: rgb(85, 145, 87);
    border: none;
    border-radius: 1rem;
  }
  </style><template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <dialog open>
    <form action="?" method="dialog">
      <div class="section">
        <div class="form-elements">
          <label for="username">Username</label>
          <input type="text" name="username" />
        </div>
        <div class="form-elements">
          <label for="vorname">Vorname</label>
          <input type="text" name="vorname" />
          <label for="nachname">Nachname</label>
          <input type="text" name="nachname" />
        </div>
      </div>
      <div class="section">
        <div class="form-elements">
          <label for="strasse">Strasse</label>
          <input type="text" name="strasse" />
        </div>
        <div class="form-elements">
          <label for="plz">PLZ</label>
          <input type="text" name="plz" />
          <label for="ort">Ort</label>
          <input type="text" name="ort" />
        </div>
      </div>
      <div class="section">
        <div class="form-elements">
          <label for="lehrjahr">Lehrjahr</label>
          <input type="text" name="lehrjahr" />
        </div>
      </div>
      <div class="form-elements">
        <label for="email">E-Mail</label>
        <input type="email" name="email" />
      </div>
      <div class="form-elements">
        <label for="pwd">Passwort</label>
        <input type="text" name="pwd" />
      </div>
      <div class="form-elements">
        <button type="submit">Submit</button>
      </div>
    </form>
  </dialog>
</template>
<style lang="scss">
.section {
  margin-bottom: 20px;
}
.form-elements {
  display: flex;
  label,
  input {
    margin-bottom: 20px;
  }
  label {
    padding-right: 10px;
    padding-left: 10px;
    font-weight: bold;
    width: 70px;
    align-self: flex-end;
  }
  input {
    width: auto;
    margin-right: 30px;
    border-radius: 5px;
    padding: 5px 10px;
  }
}
button {
  margin-left: 90px;
  height: 30px;
  width: 185px;
  border-radius: 5px;
  padding: 5px 10px;
}
dialog {
  z-index: 10;
  margin-top: 10px;
  background: rgb(85, 145, 87);
  border: none;
  border-radius: 1rem;
}
</style>