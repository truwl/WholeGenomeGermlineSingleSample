```
curl -X GET --header "Accept: application/json"    -v "localhost:8000/engine/v1/version"
#reveal cromwell version
curl -X POST --header "Accept: application/json"    -v "localhost:8000/api/workflows/v1" -F workflowSource=@WholeGenomeGermlineSingleSample_v2.3.1.wdl -F workflowInputs=@wgs.inputs.json -F workflowDependencies=@WholeGenomeGermlineSingleSample_v2.3.1.zip
#get the job hash
curl -X GET --header "Accept: application/json"    -v "localhost:8000/api/workflows/v1/<job_hash>/metadata"
curl -X GET --header "Accept: application/json"    -v "localhost:8000/api/workflows/v1/<job_hash>/status"
```