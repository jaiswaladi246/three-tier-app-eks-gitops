
# Architecture

## Request path

Traffic arrives at an Application Load Balancer provisioned by the AWS
Load Balancer Controller. The ALB routes to a ClusterIP service, which
fronts the application pods. The pods read database connection details
from environment variables supplied by a Kubernetes secret.

## Environment promotion

QA and production run the same container image. The image is built once,
tested in QA, and then retagged for production rather than rebuilt.

## Why retag rather than rebuild

Rebuilding produces a different artifact from the one that passed testing,
even when the source is identical, because base images and transitive
dependencies move underneath you. Retagging guarantees that what ships is
what was tested.
Test
