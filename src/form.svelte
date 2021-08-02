<script lang="ts">
    import '@shoelace-style/shoelace/dist/themes/base.css'
  import 'medblocks-ui'
  import './tailwind.css'
  import axios from  "axios"
   function Click(e:any)
  {
    console.log(e.target.data)
    
  }
  </script>
    <h1 class="text-2xl font-semibold font-sans">Patient Registration Form</h1>
    <div >
    <mb-form class="flex flex-col gap-5" on:mb-submit={Click}>
      <mb-context path="resourceType" data="patient"></mb-context>
      <mb-input path="name[0].given" label="Name"></mb-input>
      <mb-input  Label="Age" path="age"></mb-input>
      <mb-date path="birthdate" label="Date of Birth"></mb-date>
      <div  >
        <mb-buttons type="code" label="Gender" path="gender">
        <mb-option label="Male" value="male"></mb-option>
        <mb-option label="Female" value="female"></mb-option>
        <mb-option label="Other" value="other"></mb-option>
      </mb-buttons>
      </div>
      <mb-input label="Aadhar No." path="identifier[0].value"></mb-input>
      <mb-input path="telecome[0].value" label="Phone No."></mb-input>
      <mb-input Label="Address" textarea path="address[0].text"></mb-input>
      <div >
      <mb-buttons type="code" label="Covid Test" path="covid test">
        <mb-option label="Antigen" value="antigen"></mb-option>
        <mb-option label="RTPCR" value="RTPCR"></mb-option>
        <mb-option label="None" value="none"></mb-option>
      </mb-buttons></div>
      <mb-select path="symptom" type="code" label="Symptoms/Signs" multiple>
        <mb-option value="fever" label="Fever"></mb-option>
        <mb-option value="fatigue" label="Fatigue"></mb-option>
        <mb-option value="drycough" label="Dry cough"></mb-option>
        <mb-option value="nasalCong" label="Nasal congestion"></mb-option>
        <mb-option value="nasaldischarge" label="Nasal Discharge"></mb-option>
        <mb-option value="sorethroat" label="Sore Throat"></mb-option>
        <mb-option value="musclepain" label="Muscle Pain"></mb-option>
        <mb-option value="shrtnessO2" label="Shortness of breath"></mb-option>
        <mb-option value="diarrhea" label="Diarrhea"></mb-option>
      </mb-select>
      <mb-input label="Medication" path="medication" ></mb-input>
      <mb-input label="Cormobodities" path="cormobodities" ></mb-input>
      <mb-input label="SpO2 Level" path="SpO2 level" ></mb-input>
      <mb-input label="Allergic To" path="allergy"></mb-input>         
      <div >
      <mb-buttons label="Immunization" type="code" path="Immunization">
        <mb-option value="dose1" label="Dose-1"></mb-option>
        <mb-option value="dose2" label="Dose-2"></mb-option>
        <mb-option value="none" label="None"></mb-option>
      </mb-buttons></div>
      
      <mb-submit>
         <sl-button type="info">Submit</sl-button>
       </mb-submit>
    </mb-form>
    </div>
