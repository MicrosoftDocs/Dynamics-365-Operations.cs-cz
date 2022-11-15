---
title: Rozšiřitelnost výčtu genderové základny
description: Tento článek poskytuje přehled rozšiřitelnosti výčtu genderové základny.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749309"
---
# <a name="gender-base-enum-extensibility"></a>Rozšiřitelnost výčtu genderové základny

Výčet **Gender** je nyní rozšiřitelný. Tento článek popisuje změny, které musíte provést v základně kódu, pokud plánujete rozšíření výčtu **Gender**.

## <a name="gender-vs-hcmpersongender"></a>Gender vs. HcmPersonGender

Pro hodnoty Gender existují dva výčty:

- **Gender** (platforma aplikace)
- **HcmPersonGender** (PersonnelManagement)

Výčet **Gender** používá napříč Microsoft Dynamics 365 Finance, kdežto **HcmPersonGender** je specifická pro funkci správy lidského kapitálu (HCM). Pokud používáte funkci HCM a provedete nějaké změny výčtu **Gender**, měli byste zvážit provedení stejných změn v **HcmPersonGender**. Pokud například přidáte **Transgender** k výčtu **Gender**, přidejte **Transgender** k výčtu **HcmPersonGender** také.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (třída)

Nová třída **HcmPersonGenderTranformUtil** byla vytvořena, aby umožňovala překlad mezi dvěma základními enumerátory. V této třídě existují dvě metody: **convertGenderToHcmPersonGender** a **convertHcmPersonGenderToGender**. Měli byste vytvořit rozšíření pomocí třídy **Chain of Command** nebo **manipulátory událostí** a rozšířit obě metody o mapování nových hodnot, které jsou přidány do kteréhokoli základního výčtu.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (třída)

**PayrollStateWageTaxPrepDP** je třída poskytovatele dat pro sestavu SQL Server Reporting Services (SSRS) **Payroll State Wage Tax Prep**. Pro Spojené státy jsou k dispozici tři hodnoty: **Muž**, **Žena** a **Nespecifikováno**. Při metodě **populatePayrollStateWageTaxPrepTmp** existuje příkaz switch, který se používá k mapování hodnoty výčtu **HcmPersonGender** do jednoho ze tří polí: **IsMale**, **IsFemale** nebo **IsUnspecifiedGender**. Výchozí hodnota pro příkaz switch je **IsUnspecifiedGender**. Pokud do výčtu **HcmPersonGender** přidáte hodnoty pro jiné mapování, musíte vytvořit rozšíření pomocí třídy **Chain of Command** nad metodou **populatePayrollStateWageTaxPrepTmp** pro změnu hodnoty podle potřeby.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (třída)

Integrační třída **smmOutlookSync_Contact** spojuje hodnoty do a z **Outlook** a **Kontaktní osoby**. **Outlook** podporuje tři hodnoty: **Muž**, **Žena** a **Nespecifikováno**. Třída má dvě metody, které vám pomohou s mapováním **Gender** na **OutlookGenders**. Výchozí metoda je **NonSpecific/UnSpecified**. Pokud vytváříte další hodnoty pro výčet **Gender** měli byste vytvořit rozšíření použitím třídy **Chain of Command** pro obě metody provést mapování podle potřeby.
