---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

- Practice deploying AWS Storage Gateway and Amazon FSx (SSD/HDD Multi-AZ).
- Practice Amazon S3 Static Website Hosting, CloudFront, S3 Versioning, and Cross-Region Replication.
- Learn Security & Identity concepts on AWS: IAM, Cognito, AWS Organizations, Identity Center, and KMS.
- Practice automating EC2 management tasks using AWS Lambda and sending alerts via Slack Incoming Webhooks.
- Learn resource tagging management, Resource Groups, and Tag-based access control (TBAC) in IAM.

### Tasks to be carried out this week:

<table> 
  <thead>
    <tr>
      <th style="text-align:center;">Day</th>
      <th style="text-align:center;">Date</th>
      <th style="text-align:center;">Task</th>
      <th style="text-align:center;">Reference Material</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">2</td>
      <td style="text-align:center;">04/05/2026</td>
      <td>
        <ul>
          <li> <strong>Storage Gateway:</strong> Create Storage Gateway, File Share, and mount File Share to local machine. </li>
          <li> <strong>Amazon FSx:</strong> Create SSD/HDD Multi-AZ file system, configure quotas, shadow copies, and adjust throughput/storage. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">05/05/2026</td>
      <td>
        <ul>
          <li> <strong>Amazon S3 & CloudFront:</strong> Configure Static Website, block public access, integrate CloudFront CDN, configure Versioning, object migration, and Cross-Region Replication (CRR). </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">06/05/2026</td>
      <td>
        <ul>
          <li> <strong>Security & Identity:</strong> Study Shared Responsibility Model, IAM, Cognito, AWS Organizations, Identity Center, and KMS. </li>
          <li> <strong>Security Hub:</strong> Enable and monitor security compliance benchmark scores. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">07/05/2026</td>
      <td>
        <ul>
          <li> <strong>Slack Integration & Lambda:</strong> Create VPC, Security Group, EC2 Instance; configure Slack Incoming Webhooks. </li>
          <li> <strong>Automation:</strong> Create Lambda Role and script Lambda function to automatically start/stop EC2 instances. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">08/05/2026</td>
      <td>
        <ul>
          <li> <strong>Tagging & Resource Groups:</strong> Filter resources by tags via Console/CLI and manage Resource Groups. </li>
          <li> <strong>Advanced IAM:</strong> Create IAM Users, Policies, Roles, test Switch Role, and configure Tag-based access control (TBAC) for EC2 across Tokyo and North Virginia. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/">FCAJ Documentation</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Week 3 Achievements:

- **Storage Gateway & Amazon FSx**: Practiced deploying Storage Gateway, creating File Share, and mounting to local device. Practiced setting up Amazon FSx file systems (SSD/HDD Multi-AZ), configuring quotas, shadow copies, data deduplication, and testing throughput/storage scaling.

- **S3 Storage Optimization & CloudFront Content Delivery**: Practiced static web hosting on S3, public access blocking, CloudFront CDN integration, S3 Versioning management, object lifecycle transitions, and Cross-Region Replication (CRR).

- **Security & Identity Management on AWS**: Studied Shared Responsibility Model, IAM, Cognito, AWS Organizations, Identity Center, KMS, and practiced monitoring security compliance scores on AWS Security Hub.

- **Automation & Advanced Access Control**: Practiced writing Lambda functions for automated EC2 start/stop operations with notifications via Slack Incoming Webhooks. Practiced resource tagging management via Console/CLI, creating Resource Groups, configuring Switch Role, and testing Tag-based access control (TBAC).

- **Learning Progress**: Completed watching and studying videos 121 to 186 in the *First Cloud Journey Bootcamp 2025* series by AWS Study Group.






