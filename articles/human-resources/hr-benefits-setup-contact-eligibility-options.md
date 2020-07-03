---
title: Konfigurace možností způsobilosti osobních kontaktů
description: Nakonfigurujte možnosti způsobilosti osobních kontaktů v Microsoft Dynamics 365 Human Resources. Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68364b0cc1c579a3ee9813474c9d3f6e4df1c05d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430755"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurace možností způsobilosti osobních kontaktů

Tento článek vysvětluje, jak konfigurovat typy osobních kontaktů, které mají být použity ve výhodách v aplikaci Microsoft Dynamics 365 Human Resources. Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Možnosti nároků na osobní kontakty**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Možnost způsobilosti** | Jedinečný název nebo kód možnosti nároku pro identifikaci možnosti nároku. |
   | **Popis** | Stručný popis možnosti nároku. |
   | **Kód způsobilosti kontaktu** | Systémový kód, který nejlépe popisuje možnost osobní způsobilosti. Lze vybrat následující možnosti: <ul><li>Vztah</li><li>Student</li><li>Rodinný příslušník nad věkovým limitem</li><li>Rodinný příslušník s postižením nad věkovým limitem</li></ul> |
   | **Stav** | Stav možnosti nároku. Pokud je stav možnosti nároku nastaven na neaktivní, nemůžete vybrat možnost nároku na osobní kontakt pro osobní kontakty. |
   | **Vztah** | Určuje vztah mezi osobním kontaktem a zaměstnancem. Toto pole je aktivní pouze v případě, že je kód nároku na kontakt nastavený na vztah. |
   | **Věk** | Maximální stáří vhodného osobního kontaktu pro plán zaměstnaneckých výhod. Toto pole je aktivní pouze v případě, že vyberete vztah. Tento věk se porovnává s vypočítaným stářím osobního kontaktu. Vypočítaný věk je: (datum disponibility – datum narození osobního kontaktu / 365). Toto číslo je vždy celé číslo. |

4. Zvolte **Uložit**. 
