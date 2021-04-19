---
title: Udržování kusovníku pro model konfigurace produktu
description: Spuštění této procedury vyžaduje stávající model konfigurace produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49aa17aa376f8536e9d2290292f877d314c2c078
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818006"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Udržování kusovníku pro model konfigurace produktu

[!include [banner](../../includes/banner.md)]

Spuštění této procedury vyžaduje stávající model konfigurace produktu. Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.


## <a name="add-a-bom-line"></a>Přidání řádku kusovníku
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro tuto proceduru vyberte špičkový reproduktor.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Rozbalte sekci Řádky kusovníku.
6. Klepněte na možnost Přidat.
7. Zadejte hodnotu do pole Název.
8. Zadejte nějakou hodnotu do pole Popis.
9. Klikněte na položku Uložit.

## <a name="add-bom-line-details"></a>Přidání podrobností řádku kusovníku
1. Klepněte na podrobnosti řádku kusovníku.
2. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Můžete vybrat zboží M0055.  
    * Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.  
3. Zaškrtněte políčko položky Nastavit.
4. Vyberte možnost Ano v poli Výpočet.
    * Nastavení vlastností výpočtu na hodnotu Ano zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.  
5. Klikněte na záložku Nastavení.
6. Zaškrtněte políčko položky Nastavit.
7. Zadejte číslo do pole Množství.
    * Pole množství určuje množství zboží, které bude zahrnuto v kusovníku. Může se jednat o zřejmého uchazeče pro mapování atributů.  
8. Klepněte na kartu Dimenze.
    * Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.  
9. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]