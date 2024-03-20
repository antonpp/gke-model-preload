# gke-model-preload

```bash
kubectl apply -f pvc.yaml # create pvc where we'll download the model
kubectl apply -f load-model-job.yaml # mount the pvc and download model
kubectl logs -f jobs/load-model-job-whisper-base # check logs
kubectl apply -f test-model-job-preload.yaml # mount pvc in reodOnly and test loading time
kubectl logs -f jobs/test-model-job-whisper-base # check logs
```