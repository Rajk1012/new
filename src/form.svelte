

<script lang="ts">
import '@shoelace-style/shoelace/dist/themes/base.css'
import 'medblocks-ui'
import './tailwind.css'
import axios from  "axios"
 function Click(e:any)
{
  console.log(e.target.data)
  
}
// var form = document.querySelector('mb-form')
//       form.cdr = axios.create({baseURL: "http://localhost:8080/ehrbase/rest/eci/v1"})
//      form.template = "Covid.form.v1"
//       form.ehr = "5338b7cf-947c-4a31-bd51-57e3e8d8e237"

//     form.addEventListener('submit',(e)=>{
//       form.post(e.detail).then(r=>alert(JSON.stringify(r)))
//     })

</script>
<div class="container mx-auto sm:gx-8 max-w-5xl py-10">
  <h1 class="text-2xl font-semibold font-sans">Patient Registration Form</h1>
  <div >
  <mb-form class="flex flex-col gap-5" on:mb-submit={Click}>
    <mb-context path="resourceType" data="patient"></mb-context>
    <mb-input path="name[0].given" label="Name"></mb-input>

   <mb-input path="encounter_1/age/age_category" label="Age"></mb-input>
    <mb-date path="birthdate" label="Date of Birth"></mb-date>
    <div  >
      <mb-buttons type="value" label="Gender" path="gender">
      <mb-option label="Male" value="male"></mb-option>
      <mb-option label="Female" value="female"></mb-option>
      <mb-option label="Other" value="other"></mb-option>
    </mb-buttons>
    </div>
    <mb-input label="Aadhar No." path="identifier[0].value"></mb-input>
    <mb-input path="telecome[0].value" label="Phone No."></mb-input>
    <mb-input Label="Address" textarea path="address[0].text"></mb-input>
    <div >
    <mb-buttons type="value" label="Covid Test" path="covid test">
      <mb-option label="Antigen" value="antigen"></mb-option>
      <mb-option label="RTPCR" value="RTPCR"></mb-option>
      <mb-option label="None" value="none"></mb-option>
    </mb-buttons></div>
    <mb-context path="covid.form.v1/context/start_time"></mb-context>
<mb-context path="covid.form.v1/context/setting"></mb-context>
<mb-select path="covid.form.v1/clinical_background/covid_19_admission/hospital_admission_status" label="Hospital admission status">
            <mb-option value="at0003" label="YES"></mb-option>
<mb-option value="at0004" label="NO"></mb-option>
<mb-option value="at0005" label="UNKNOWN"></mb-option>
          </mb-select>
<mb-date time path="covid.form.v1/clinical_background/covid_19_admission/date_first_admitted" label="Date first admitted"></mb-date>
<mb-context path="covid.form.v1/clinical_background/covid_19_admission/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/covid_19_admission/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/covid_19_admission/subject"></mb-context>


<mb-input path="covid.form.v1/clinical_background/age/comment" label="Comment"></mb-input>
<mb-context path="covid.form.v1/clinical_background/age/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/age/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/age/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/age/subject"></mb-context>
<mb-input path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/screening_purpose" label="Screening purpose"></mb-input>
<mb-select path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/presence_of_any_symptoms_or_signs" label="Presence of any symptoms or signs?">
            <mb-option value="at0031" label="Present"></mb-option>
<mb-option value="at0032" label="Absent"></mb-option>
<mb-option value="at0033" label="Unknown"></mb-option>
          </mb-select>
<mb-date time path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/onset_of_any_symptoms_or_signs" label="Onset of any symptoms or signs"></mb-date>
<mb-input path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/description" label="Description"></mb-input>
<mb-input path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/specific_symptom_sign:0/symptom_or_sign_name" label="Symptom or sign name"></mb-input>
<mb-select path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/specific_symptom_sign:0/presence" label="Presence?">
            <mb-option value="at0023" label="Present"></mb-option>
<mb-option value="at0024" label="Absent"></mb-option>
<mb-option value="at0027" label="Unknown"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/specific_symptom_sign:0/comment" label="Comment"></mb-input>
<mb-input path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/overall_comment" label="Overall comment"></mb-input>
<mb-context path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/symptom_sign_screening_questionnaire/subject"></mb-context>
<mb-input path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/screening_purpose" label="Screening purpose"></mb-input>
<mb-select path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/presence_of_any_conditions" label="Presence of any conditions?">
            <mb-option value="at0031" label="Present"></mb-option>
<mb-option value="at0032" label="Absent"></mb-option>
<mb-option value="at0033" label="Unknown"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/specific_condition:0/condition_name" label="Condition name"></mb-input>
<mb-select path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/specific_condition:0/presence" label="Presence?">
            <mb-option value="at0023" label="Present"></mb-option>
<mb-option value="at0024" label="Absent"></mb-option>
<mb-option value="at0027" label="Unknown"></mb-option>
          </mb-select>
<mb-date time path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/specific_condition:0/onset" label="Onset"></mb-date>
<mb-input path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/specific_condition:0/comment" label="Comment"></mb-input>

<mb-select path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/pregnancy_gestation/valued_text_value" label="">
            <mb-option value="at0036" label="First trimester"></mb-option>
<mb-option value="at0037" label="Second trimester"></mb-option>
<mb-option value="at0038" label="Third trimester"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/overall_comment" label="Overall comment"></mb-input>
<mb-context path="covid.form.v1/clinical_background/condition_screening_questionnaire/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/condition_screening_questionnaire/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/condition_screening_questionnaire/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/condition_screening_questionnaire/subject"></mb-context>
<mb-input path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/screening_purpose" label="Screening purpose"></mb-input>
<mb-input path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/specific_management_treatment_activity:0/activity_name" label="Activity name"></mb-input>
<mb-select path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/specific_management_treatment_activity:0/actioned" label="Actioned?">
            <mb-option value="at0023" label="Actioned"></mb-option>
<mb-option value="at0024" label="Not actioned"></mb-option>
<mb-option value="at0027" label="Unknown"></mb-option>
          </mb-select>
<mb-date time path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/specific_management_treatment_activity:0/date_actioned" label="Date actioned"></mb-date>
<mb-input path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/specific_management_treatment_activity:0/comment" label="Comment"></mb-input>
<mb-input path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/overall_comment" label="Overall comment"></mb-input>
<mb-context path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/management_treatment_screening_questionnaire/subject"></mb-context>
<mb-quantity default="Cel" path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/temperature" label="Temperature">
                <mb-unit unit="Cel" label="Cel"></mb-unit>
<mb-unit unit="[degF]" label="[degF]"></mb-unit>
            </mb-quantity>
<mb-input path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/comment" label="Comment"></mb-input>
<mb-select path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/body_exposure" label="Body exposure">
            <mb-option value="at0031" label="Naked"></mb-option>
<mb-option value="at0032" label="Reduced clothing/bedding"></mb-option>
<mb-option value="at0033" label="Appropriate clothing/bedding"></mb-option>
<mb-option value="at0034" label="Increased clothing/bedding"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/description_of_thermal_stress" label="Description of thermal stress"></mb-input>

<mb-input path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/confounding_factors:0" label="Confounding factors"></mb-input>
<mb-context path="covid.form.v1/clinical_background/vital_signs/body_temperature/any_event:0/time"></mb-context>
<mb-select path="covid.form.v1/clinical_background/vital_signs/body_temperature/location_of_measurement" label="Location of measurement">
            <mb-option value="at0025" label="Rectum"></mb-option>
<mb-option value="at0024" label="Axilla"></mb-option>
<mb-option value="at0023" label="Ear canal"></mb-option>
<mb-option value="at0061" label="Forehead"></mb-option>
<mb-option value="at0022" label="Mouth"></mb-option>
<mb-option value="at0026" label="Nasopharynx"></mb-option>
<mb-option value="at0027" label="Urinary bladder"></mb-option>
<mb-option value="at0028" label="Intravascular"></mb-option>
<mb-option value="at0043" label="Skin"></mb-option>
<mb-option value="at0051" label="Vagina"></mb-option>
<mb-option value="at0054" label="Oesophagus"></mb-option>
<mb-option value="at0055" label="Inguinal skin crease"></mb-option>
<mb-option value="at0060" label="Temple"></mb-option>
          </mb-select>
<mb-context path="covid.form.v1/clinical_background/vital_signs/body_temperature/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/body_temperature/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/body_temperature/subject"></mb-context>
<mb-select path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/presence" label="Presence">
            <mb-option value="at0063" label="Present"></mb-option>
<mb-option value="at0064" label="Not detected"></mb-option>
          </mb-select>
<mb-quantity default="/min" path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/rate" label="Rate">
                <mb-unit unit="/min" label="/min"></mb-unit>
            </mb-quantity>
<mb-select path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/regularity" label="Regularity">
            <mb-option value="at0006" label="Regular"></mb-option>
<mb-option value="at0007" label="Irregular"></mb-option>
          </mb-select>
<mb-select path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/depth" label="Depth">
            <mb-option value="at0017" label="Normal"></mb-option>
<mb-option value="at0018" label="Shallow"></mb-option>
<mb-option value="at0019" label="Deep"></mb-option>
<mb-option value="at0025" label="Variable"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/clinical_description" label="Clinical description"></mb-input>
<mb-input path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/clinical_interpretation:0" label="Clinical interpretation"></mb-input>
<mb-input path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/comment" label="Comment"></mb-input>
<mb-select path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/body_position" label="Body position">
            <mb-option value="at0066" label="Standing/upright"></mb-option>
<mb-option value="at0067" label="Sitting"></mb-option>
<mb-option value="at0068" label="Reclining"></mb-option>
<mb-option value="at0069" label="Lying"></mb-option>
<mb-option value="at0071" label="Prone"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/confounding_factors:0" label="Confounding factors"></mb-input>
<mb-context path="covid.form.v1/clinical_background/vital_signs/respiration/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/respiration/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/respiration/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/respiration/subject"></mb-context>

<mb-input path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/any_event:0/interpretation:0" label="Interpretation"></mb-input>
<mb-input path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/any_event:0/confounding_factors:0" label="Confounding factors"></mb-input>
<mb-context path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/vital_signs/pulse_oximetry/subject"></mb-context>
<mb-select path="covid.form.v1/clinical_background/travel_screening_questionnaire/any_event:0/travel" label="Travel?">
            <mb-option value="at0006" label="Yes"></mb-option>
<mb-option value="at0005" label="No"></mb-option>
<mb-option value="at0027" label="Unknown"></mb-option>
          </mb-select>
<mb-select path="covid.form.v1/clinical_background/travel_screening_questionnaire/any_event:0/domestic_international" label="Domestic/international">
            <mb-option value="at0028" label="Domestic travel"></mb-option>
<mb-option value="at0029" label="International travel"></mb-option>
<mb-option value="at0030" label="Domestic and international travel"></mb-option>
          </mb-select>
<mb-context path="covid.form.v1/clinical_background/travel_screening_questionnaire/any_event:0/time"></mb-context>
<mb-context path="covid.form.v1/clinical_background/travel_screening_questionnaire/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/travel_screening_questionnaire/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/travel_screening_questionnaire/subject"></mb-context>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/test_name" label="Test name"></mb-input>
<mb-select path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/overall_test_status" label="Overall test status">
            <mb-option value="at0107" label="Registered"></mb-option>
<mb-option value="at0037" label="Partial"></mb-option>
<mb-option value="at0120" label="Preliminary"></mb-option>
<mb-option value="at0038" label="Final"></mb-option>
<mb-option value="at0040" label="Amended"></mb-option>
<mb-option value="at0115" label="Corrected"></mb-option>
<mb-option value="at0119" label="Appended"></mb-option>
<mb-option value="at0074" label="Cancelled"></mb-option>
<mb-option value="at0116" label="Entered in error"></mb-option>
          </mb-select>
<mb-date time path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/overall_test_status_timestamp" label="Overall test status timestamp"></mb-date>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/diagnostic_service_category" label="Diagnostic service category"></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/clinical_information_provided" label="Clinical information provided"></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/conclusion" label="Conclusion"></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/test_diagnosis:0" label="Test diagnosis"></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/comment:0" label="Comment"></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/confounding_factors:0" label="Confounding factors"></mb-input>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/any_event:0/time"></mb-context>

<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/laboratory_internal_identifier/text_value" label=""></mb-input>
<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_request_details:0/original_test_requested_name:0" label="Original test requested name"></mb-input>

<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_request_details:0/requester_order_identifier/text_value" label=""></mb-input>

<mb-input path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_request_details:0/receiver_order_identifier/text_value" label=""></mb-input>
<mb-checkbox path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/point-of-care_test" label="Point-of-care test"></mb-checkbox>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/valued_text_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/text_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/multimedia_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/parsable_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/state_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/boolean_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/identifier_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/uri_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/ehr_uri_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/duration_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/quantity_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/count_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/proportion_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/date_time_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/date_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/time_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/ordinal_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/test_method/scale_value"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/language"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/encoding"></mb-context>
<mb-context path="covid.form.v1/clinical_background/lab_testing/laboratory_test_result/subject"></mb-context>
<mb-select path="covid.form.v1/assessment/covid-19_infection_risk_assessment/health_risk" label="Health risk">
            <mb-option value="at0.1" label="COVID-19 Risk assessment"></mb-option>
          </mb-select>
<mb-select path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/risk_factor" label="Risk factor">
            <mb-option value="at0.9" label="Contact with confirmed Covid-19 case"></mb-option>
<mb-option value="at0.14" label="Potential contact exposure based on location"></mb-option>
<mb-option value="at0.10" label="Contact with suspected case/ pneumonia case"></mb-option>
<mb-option value="at0.13" label="Contact with severe, unexplained respiratory disease"></mb-option>
<mb-option value="at0.11" label="Contact with birds in China"></mb-option>
<mb-option value="at0.12" label="Contact with confirmed human case of Avian flu in China"></mb-option>
<mb-option value="at0.18" label="Needs admission for respiratory disease"></mb-option>
<mb-option value="at0.19" label="Other household members are ill"></mb-option>
<mb-option value="at0.20" label="Household members with travel exposure"></mb-option>
          </mb-select>
<mb-select path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/presence" label="Presence">
            <mb-option value="at0018" label="Present"></mb-option>
<mb-option value="at0019" label="Absent"></mb-option>
<mb-option value="at0.15" label="Unknown"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/description" label="Description"></mb-input>
<mb-date time path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/date_identified" label="Date identified"></mb-date>
<mb-checkbox path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/mitigated" label="Mitigated"></mb-checkbox>

<mb-input path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_factors:0/comment" label="Comment"></mb-input>
<mb-select path="covid.form.v1/assessment/covid-19_infection_risk_assessment/risk_assessment" label="Risk assessment">
            <mb-option value="at0.16" label="Low risk"></mb-option>
<mb-option value="at0.17" label="High risk"></mb-option>
          </mb-select>
<mb-select path="covid.form.v1/assessment/covid-19_infection_risk_assessment/assessment_type" label="Assessment type">
            <mb-option value="at0021" label="Relative risk"></mb-option>
<mb-option value="at0022" label="Absolute risk"></mb-option>
          </mb-select>

<mb-input path="covid.form.v1/assessment/covid-19_infection_risk_assessment/rationale" label="Rationale"></mb-input>
<mb-input path="covid.form.v1/assessment/covid-19_infection_risk_assessment/comment" label="Comment"></mb-input>
<mb-date time path="covid.form.v1/assessment/covid-19_infection_risk_assessment/last_updated" label="Last updated"></mb-date>
<mb-input path="covid.form.v1/assessment/covid-19_infection_risk_assessment/assessment_method" label="Assessment method"></mb-input>
<mb-context path="covid.form.v1/assessment/covid-19_infection_risk_assessment/language"></mb-context>
<mb-context path="covid.form.v1/assessment/covid-19_infection_risk_assessment/encoding"></mb-context>
<mb-context path="covid.form.v1/assessment/covid-19_infection_risk_assessment/subject"></mb-context>
<mb-input path="covid.form.v1/conclusion/problem_diagnosis/problem_diagnosis_name" label="Problem/Diagnosis name"></mb-input>
<mb-input path="covid.form.v1/conclusion/problem_diagnosis/clinical_description" label="Clinical description"></mb-input>
<mb-input path="covid.form.v1/conclusion/problem_diagnosis/body_site:0" label="Body site"></mb-input>
<mb-date time path="covid.form.v1/conclusion/problem_diagnosis/date_time_of_onset" label="Date/time of onset"></mb-date>
<mb-date time path="covid.form.v1/conclusion/problem_diagnosis/date_time_clinically_recognised" label="Date/time clinically recognised"></mb-date>
<mb-select path="covid.form.v1/conclusion/problem_diagnosis/severity" label="Severity">
            <mb-option value="at0047" label="Mild"></mb-option>
<mb-option value="at0048" label="Moderate"></mb-option>
<mb-option value="at0049" label="Severe"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/conclusion/problem_diagnosis/course_description" label="Course description"></mb-input>
<mb-date time path="covid.form.v1/conclusion/problem_diagnosis/date_time_of_resolution" label="Date/time of resolution"></mb-date>
<mb-select path="covid.form.v1/conclusion/problem_diagnosis/diagnostic_certainty" label="Diagnostic certainty">
            <mb-option value="at0074" label="Suspected"></mb-option>
<mb-option value="at0075" label="Probable"></mb-option>
<mb-option value="at0076" label="Confirmed"></mb-option>
          </mb-select>
<mb-input path="covid.form.v1/conclusion/problem_diagnosis/comment" label="Comment"></mb-input>
<mb-date time path="covid.form.v1/conclusion/problem_diagnosis/last_updated" label="Last updated"></mb-date>
<mb-context path="covid.form.v1/conclusion/problem_diagnosis/language"></mb-context>
<mb-context path="covid.form.v1/conclusion/problem_diagnosis/encoding"></mb-context>
<mb-context path="covid.form.v1/conclusion/problem_diagnosis/subject"></mb-context>
<mb-context path="covid.form.v1/category"></mb-context>
<mb-context path="covid.form.v1/language"></mb-context>
<mb-context path="covid.form.v1/territory"></mb-context>
<mb-context path="covid.form.v1/composer"></mb-context>
    <mb-submit>
       <sl-button type="info">Submit</sl-button>
     </mb-submit>
  </mb-form>
  </div>
</div>
