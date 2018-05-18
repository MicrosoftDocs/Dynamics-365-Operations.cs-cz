---
title: "Vztahy předmětu servisu"
description: "Mezi předmětem servisu a servisní smlouvou či zakázkou můžete vytvářet vztahy předmětů servisu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: cs-cz
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a>Vztahy předmětu servisu 

[!include [banner](../includes/banner.md)]

Mezi předmětem servisu a servisní smlouvou či zakázkou můžete vytvářet vztahy předmětů servisu. Při vytvoření vztahu připojíte předmět servisu k servisní smlouvě nebo zakázce.

Po vytvoření vztahu můžete předmět servisu připojit k libovolným řádkům servisní smlouvy nebo zakázky.

## <a name="template-boms"></a>Kusovníky šablony

Je také možné určit šablonu kusovníku pro vztah předmětu. Šablona kusovníku představuje kusovník předmětu, u kterého provádíte servis. Jestliže při servisním zásahu vyměníte součástku předmětu servisu, můžete tuto změnu zaregistrovat do servisního kusovníku ve formuláři Předměty servisu.

## <a name="example"></a>Příklad

Vytváříte servisní smlouvu pro servis dvou výtahů u zákazníka.
Identifikátor servisní smlouvy je SAL-001.

Výtahy jsou nastaveny ve formuláři Předměty servisu jako předměty EL-S/1000 a EL-L/1000.

Předměty servisu EL-S/1000 a EL-L/1000 jste připojili k servisní smlouvě.

Chcete zaregistrovat změny kusovníku předmětu servisu, ke kterým došlo při výměně součástek předmětu. Připojte servisní kusovník ke vztahu předmětu servisu tak, jak je popsáno v následující tabulce.

| Předmět servisu | Vztah – servisní smlouva | Servisní kusovník   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Protože smlouva obsahuje vztahy předmětů servisu, můžete nyní vytvořit řádky servisní smlouvy s těmito předměty podle popisu zobrazeného v následující tabulce.

| typ transakce | Kategorie           | Předmět servisu |
|------------------|--------------------|----------------|
| Hodina             | Kontrola         | EL-S/1000      |
| Hodina             | Čištění převodovky  | EL-S/1000      |
| Položka             | Čistící materiál | EL-S/1000      |
| Hodina             | Kontrola         | EL-L/1000      |
| Hodina             | Čištění převodovky   | EL-L/1000      |
| Položka             | Čistící materiál | EL-L/1000      |

Při servisním zásahu je nutné vyměnit převodovku výtahu EL-S/1000. Otevřením nástroje Návrhář kusovníku pomocí vztahu předmětu servisu nastaveného pro aktuální servisní smlouvu proveďte výměnu součástky předmětu.

Otevření Návrháře kusovníku pomocí vztahu předmětu servisu

1. Servisní smlouvy
2. Dvakrát klikněte na servisní smlouvu nebo kliknutím na možnost Servisní smlouva vytvořte novou servisní smlouvu.
3. Klikněte na záložku Nastavení.
4. Chcete-li k servisní smlouvě připojit šablonu kusovníku, klikněte na položku Předměty servisu.
5. Ve formuláři Předměty servisu klikněte na tlačítko Návrhář a otevřete formulář návrháře pro úpravu šablony kusovníku.

## <a name="automatically-created-service-orders"></a>Automaticky vytvářené servisní zakázky

Vytváříte-li servisní zakázky pro servisní smlouvu automaticky, vztahy předmětů servisu ve smlouvě budou rovněž vytvořeny v servisních zakázkách.


