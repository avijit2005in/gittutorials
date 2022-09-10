# gittutorials
# 2nd commit

# Deploy object detection app on cloud 

https://www.cloudskillsboost.google/focuses/1823?parent=catalog

1. SSH cdd-crop-parts-infer gcp VM instance

2. sudo -i

3. cd $HOME

4. cd my_models

5. mkdir -p model_experiment_{n}

6. gsutil cp -r gs://tf2-crop-od-bucket/Experiment_{n}/inference_graph/ model_experiment_{n}/

7. cd /opt/my_models

8. mkdir -p model_experiment_{n}

9. cd $HOME

10. cp -a my_models/model_experiment_{n}/inference_graph/ /opt/my_models/model_experiment_{n}/

11. cp -a gittutorials/crop_parts_detection_app_p3 /opt/

12. chmod u+x /opt/crop_parts_detection_app_p3/app.py

13. cp /opt/crop_parts_detection_app_p3/object-detection.service /etc/systemd/system/

14. systemctl stop object-detection

15. systemctl daemon-reload

16. systemctl enable object-detection

17. systemctl start object-detection

18. systemctl status object-detection


###############################################################################################################################

#GCP instance commands

mkdir -p model_experiment_5

root@cdd-od-infer:~/my_models# gsutil cp -r gs://tf2-crop-od-bucket/Experiment_5/inference_graph/ model_experiment_5/

cd /opt

mkdir -p my_models

mkdir -p model_experiment_5

cd $HOME

cp -a my_models/model_experiment_5/inference_graph/ /opt/my_models/model_experiment_5/

cp -a /my_models/model_experiment_5/inference_graph/ /opt/my_models/model_experiment_5/

