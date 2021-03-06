---
title: Přijetí smíšené registrační značky
description: Toto téma popisuje, jak používat kombinovaný příjem do registračních pokladen a vytvářet práci pro více položek pomocí mobilního zařízení.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b17b3a4d704c5bfd051426e708d39022e59cc67a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810455"
---
# <a name="mixed-license-plate-receiving"></a>Přijetí smíšené registrační značky

[!include [banner](../includes/banner.md)]

Přijetí smíšené registrační značky umožňuje vytvořit registrační značku sestávající z více položek předtím, než zaregistrujete a vytvoříte odloženou práci. 

Registrační značka, která se skládá z několika položek, nemusí být rozdělená v přijímacím překladišti, kde můžete registrovat jednotlivé položky. 

Používáte-li tok související s položkou k identifikaci řádek zdrojového dokumentu, můžete naskenovat čárové kódy na ovládacím prvku položky. Pokud má čárový kód nakonfigurované množství a měrnou jednotku, položka a množství budou automaticky přidány do smíšené registrační značky a vy se vrátíte na obrazovku k naskenování jiné položky. Tímto způsobem lze rychle skenovat položky bez nutnosti provádět potvrzení při každém kroku prohledávání všech položek. 

V průběhu přijetí smíšené registrační značky můžete zobrazit seznam položek, které jsou již zkontrolovány pro registrační značku a odsud můžete upravit nebo opravit množství položky.

## <a name="where-it-applies"></a>Kdy se to používá

Kombinovaný příjem registrační značky je tok příjmu na mobilní zařízení k registraci a vytvoření práce pro více řádek / položek současně. To je užitečné, pokud přijímáte příchozí registrační značky s více položkami. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Jak nastavit příjem smíšené registrační značky
Příjem smíšené registrační značky je nastaven jako položka nabídky mobilního zařízení.

Je nutné vytvořit novou položku nabídky s prací v režimu, která nepoužívá stávající práci a používá některou z následujících metod:

- Přijetí smíšené registrační značky
- Přijetí a odložení smíšené registrační značky

Možnosti pro identifikaci řádky zdrojového dokumentu jsou položka nákupní objednávky, řádek nákupní objednávky, vratka, položka převodu objednávky a řádek převodního příkazu. Tyto volby mohou změnit pořadí příjmu u jedné registrační značky. Poslední možností je podle položky nákladu. Můžete přidat více položek do registrační značky vozidla, ale nelze přepínat mezi více náklady.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]