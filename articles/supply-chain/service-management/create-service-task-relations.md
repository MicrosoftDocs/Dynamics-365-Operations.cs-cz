---
title: Vytvoření relací servisních úloh
description: Servisní úlohy lze přidružit servisním smlouvám nebo servisním zakázkám pro popis servisní úlohy pro dokončení pro smlouvu nebo zakázku.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9e0e869f22fc6f294c2dfc35b883cafe0e4205c6269e1b1fec7b223c1a9ea6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751786"
---
# <a name="create-service-task-relations"></a>Vytvoření relací servisních úloh    

[!include [banner](../includes/banner.md)]

Servisní úlohy lze přidružit servisním smlouvám nebo servisním zakázkám pro popis servisní úlohy pro dokončení pro smlouvu nebo zakázku. Tyto informace se zobrazí technikům i zákazníkům.

## <a name="create-a-relation-with-a-service-agreement"></a>Vytvoření relace se servisní smlouvou

1.  Přejděte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.

2.  Vyberte existující servisní smlouvu nebo vytvořte novou smlouvu.

3.  V podokně akcí vyberte tlačítko **Servisní úlohy**.

4.  Ve formuláři **Servisní úlohy** vytvořte nový řádek výběrem možnosti **Nový** a pak vyberte servisní úlohu v seznamu **Servisní úloha** pro připojení servisní úlohy k servisní smlouvě.

5.  Na kartě **Popis** zadejte jakékoli interní nebo externí popisy.

6.  Zavřením formuláře uložte záznam.

Stejným způsobem vytvořte všechny relace servisních úloh pro servisní smlouvu. Nyní můžete tyto servisní úlohy zadat pro jakékoli připojené řádky smlouvy.

Relace servisní úlohy vytvořená na servisní smlouvě je k dispozici ve všech servisních zakázkách připojených k této servisní smlouvě.

## <a name="create-a-relation-with-a-service-order"></a>Vytvoření relace se servisní zakázkou

1.  Přejděte na **Správa servisu** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Vyberte existující servisní zakázku nebo vytvořte novou zakázku.

3.  V podokně akcí vyberte tlačítko **Servisní úlohy**.

4.  Ve formuláři **Servisní úlohy** vytvořte nový řádek výběrem možnosti **Nový** a pak vyberte servisní úlohu v seznamu **Servisní úloha** pro připojení servisních úloh k servisní zakázce.

5.  Na kartě **Popis** zadejte jakékoli interní nebo externí popisy.

6.  Zavřením formuláře uložte záznam.

Stejným způsobem vytvořte všechny relace servisních úloh pro servisní zakázku. Nyní můžete při vytváření řádků servisní zakázky vybrat servisní úlohu, pro kterou jste vytvořili relaci.

Relace servisní úlohy vytvořená na servisní zakázce je k dispozici na konkrétní servisní zakázce.

## <a name="see-also"></a>Viz také

[Přehled servisních úloh](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]