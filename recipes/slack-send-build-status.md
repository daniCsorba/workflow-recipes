# (iOS/Android) Slack - send build status

## Description
Send a message to Slack with the build status after a build has finished.

## Prerequisites

- You have Slack webhook set up and added to Env Vars (for example, `$SLACK_WEBHOOK`). See [Configuring Slack integration](https://devcenter.bitrise.io/en/builds/configuring-build-settings/configuring-slack-integration.html) for details.

## Instructions

1. Add the [Send a Slack message](https://www.bitrise.io/integrations/steps/slack) Step. Set the input variables:
    - **Slack Webhook URL**: for example, `$SLACK_WEBHOOK`.
    - **Target Slack channel, group or username**: for example, `#build-notifications`.
    - Check out the other optional input variables in the Workflow Editor or in the Step description.

## bitrise.yml

```yaml
- slack@3:
    inputs:
    - channel: "#build-notifications"
    - webhook_url: $SLACK_WEBHOOK
```

