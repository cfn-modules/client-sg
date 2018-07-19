[![Build Status](https://travis-ci.org/cfn-modules/client-sg.svg?branch=master)](https://travis-ci.org/cfn-modules/client-sg)
[![NPM version](https://img.shields.io/npm/v/@cfn-modules/client-sg.svg)](https://www.npmjs.com/package/@cfn-modules/client-sg)

# cfn-modules: Client Security Group

Security Group to mark traffic from client (e.g. database client).

## Install

> Install [Node.js and npm](https://nodejs.org/) first!

```
npm i @cfn-modules/client-sg
```

## Usage

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: 'cfn-modules example'
Resources:
  ClientSg:
    Type: 'AWS::CloudFormation::Stack'
    Properties:
      Parameters:
        VpcModule: !GetAtt 'Vpc.Outputs.StackName' # required
      TemplateURL: './node_modules/@cfn-modules/client-sg/module.yml'
```

## Parameters

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Default</th>
      <th>Required?</th>
      <th>Allowed values</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VpcModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/vpc">vpc module</a></td>
      <td></td>
      <td>yes</td>
      <td></td>
    </tr>
  </tbody>
</table>
