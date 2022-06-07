## Test Envoy Connectivity
### Should Succeed
curl -k https://app.skrzypek.dev
### Should NOT Succeed
curl http://app.skrzypek.dev

## Test Istio Workload Connectivity
### Should Succeed
kubectl exec -n default deployment/nginx -- curl http://app.skrzypek.dev
### Should NOT Succeed
kubectl exec -n default deployment/nginx -- curl https://app.skrzypek.dev

## Test external Gateway Connectivity
### Should Succeed
curl -k https://gate.skrzypek.dev
### Should NOT Succeed
curl http://gate.skrzypek.dev
