push-juicefs-csi-driver-chart-aws:
	@echo
	@echo "=== login to registry ==="
	aws ecr get-login-password --region $(ECR_REGION) | helm registry login $(ECR_HOST) --username $(ECR_USERNAME) --password-stdin --debug
	@echo
	@echo "=== save chart ==="
	helm chart save juicefs-csi-driver/ $(ECR_HOST)/dataos-base-charts:juicefs-csi-driver-0.14.2-d1
	@echo
	@echo "=== push chart ==="
	helm chart push $(ECR_HOST)/dataos-base-charts:juicefs-csi-driver-0.14.2-d1
	@echo
	@echo "=== logout of registry ==="
	helm registry logout $(ECR_HOST)