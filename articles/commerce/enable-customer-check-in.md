---
title: Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)
description: Toto téma popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271418"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).

Ve svých e-mailech „objednávka je připravena k vyzvednutí“ mohou organizace poskytnout odkaz nebo tlačítko, které zákazníkům umožní upozornit obchod, že jsou v areálu a čekají, až jim bude doručen jejich balíček. Zákazníci poté obdrží potvrzení o přihlášení a obchod obdrží oznámení jako úkol ve své aplikaci POS. Tento úkol slouží jako výzva prodejnímu pracovníkovi k doručení objednávky do vozidla zákazníka. Zákazník tedy nemusí vstoupit do obchodu.

Workflow přihlášení zákazníka lze také nakonfigurovat tak, aby shromažďoval od zákazníků další informace, například číslo jejich parkovacího místa, značku, model a barvu jejich vozidla a pokyny k dodání. Obsluha obchodu může tyto informace použít k usnadnění plnění objednávky.

## <a name="enable-customer-check-in"></a>Aktivace přihlášení zákazníka

Když je zapnuta funkce přihlášení zákazníka, vygeneruje Commerce ID potvrzení objednávky (označované také jako referenční číslo kanálu). Také generuje ID potvrzení objednávky pro objednávky, které jsou vytvořeny prostřednictvím prodejních míst (POS) nebo kanálů call centra. 

Chcete-li zapnout funkci přihlášení zákazníka v centrále Commerce, postupujte následovně.

1. Přejděte na **Pracovní prostory \> Správa funkcí**.
2. Vyhledejte funkci **Vygenerovat konzistentní formát ID referenčního kanálu napříč kanály**. 
3. Vyberte funkci a poté v podokně vlastností vyberte možnost **Povolit nyní**. 

## <a name="create-a-check-in-confirmation-page"></a>Vytvořte stránku s potvrzením přihlášení

Na svém webu elektronického obchodu musíte vytvořit novou stránku, která bude sloužit jako prostředí pro potvrzení přihlášení. Prostřednictvím další konfigurace může stránka také obsahovat formulář, který shromažďuje další informace od zákazníků, aby se usnadnilo plnění objednávky. Informace o tom, jak nastavit stránku a modul, najdete v části [Modul přihlášení zákazníka](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurace šablony transakčního e-mailu

Musíte přidat odkaz nebo tlačítko **Jsem tady** na šablonu pro transakční e-mail, který zákazníci obdrží, když je jejich objednávka připravena k vyzvednutí. Tímto odkazem nebo tlačítkem zákazníci upozorní obchod, že dorazili, aby si vyzvedli objednávku. 

Přidejte odkaz nebo tlačítko na šablonu, která je namapována na typ oznámení **Balení dokončeno** a způsob doručení, který používáte k plnění objednávky. V šabloně vytvořte odkaz nebo tlačítko HTML, které odkazuje na adresu URL stránky s potvrzením přihlášení, kterou jste vytvořili. Následuje příklad.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Další informace o konfiguraci e-mailových šablon najdete v tématu [Přizpůsobení transakčních e-mailů podle způsobu doručení](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>V POS je vytvořena úloha potvrzení odbavení

Poté, co zákazník upozorní obchod, že je přítomen k vyzvednutí, obdrží oznámení o potvrzení přihlášení a v seznamu úkolů v POS pro obchod, kde si zákazník vyzvedává objednávku, se vytvoří úkol. Úkol obsahuje všechny informace o zákazníkovi a objednávce, které jsou nutné pro splnění objednávky. V poli úkolu se v poli s pokyny zobrazují všechny informace, které byly od zákazníka shromážděny prostřednictvím formuláře s doplňujícími informacemi. 

## <a name="additional-resources"></a>Další prostředky

[Přihlášení k modulu vyzvednutí](check-in-pickup-module.md)
