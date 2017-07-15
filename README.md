# Project Management Application

This is a Tracking the projects and management group of people application made with Ruby on Rails during The Complete Ruby on Rails Developer Course

# Functionalities

- Sign Up
  - Free Plan no paymeny
  - Premium Plan required payment, https://stripe.com/docs/testing
  - Confirm account via email
  - Has Admin status
- Log In
- Log Out
- Profile
  - Edit and Update
- Add Members -> only Admin
  - Send confirmation email to the new member
  - The new members comfirm an email and create thier password 
  - Has User status
- Change Plan -> only Admin
  - Update Company name
  - Update Plan from Free to Premium, Require payment https://stripe.com/docs/testing
- New project -> only Admin
- Delete project -> only Admin
- Edit porject -> only Admin
- Edit Users -> only Admin
  - List User invole with project
  - List User not invole with project
  - Add User to invole with project
  - Remove User out of project
- Project
  - New Artifact, Upload file to S3 Bucket AWS
  - Delete Artifact

# Model Associations

```
User **one_to_one** Member
User **many_to_many** Project, Through: :User_Project
Project **one_to_many** Artifact
Tenant **one_to_one** Payment
Tenant **one_to_many** Project
Tenant **one_to_many** Member
```

# Technologies

- Ruby 2.3.0
- Rails 4.2.5
- gem devise
- gem milia
- gem twitter-bootstrap-rails
- gem devise-bootstrap-views
- gem bootstrap-datepicker-rails
- gem aws-sdk
- gem stripe

# Demo

Running demo at: https://saas-app-supachai.herokuapp.com
