---
title: Udržování kusovníku pro model konfigurace produktu
description: Spuštění této procedury vyžaduje stávající model konfigurace produktu.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577281"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Udržování kusovníku pro model konfigurace produktu

[!include [banner](../../includes/banner.md)]

Spuštění této procedury vyžaduje stávající model konfigurace produktu. Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.

## <a name="add-a-bom-line"></a>Přidání řádku kusovníku

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Pro tuto proceduru vyberte špičkový reproduktor.  
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Rozbalte sekci **Řádky kusovníku**.
1. Vyberte **přidat**.
1. Zadejte hodnotu do pole **Název**.
1. Zadejte hodnotu do pole **Popis**.
1. Zvolte **Uložit**.

## <a name="add-bom-line-details"></a>Přidání podrobností řádku kusovníku

1. Vyberte **Podrobnosti řádku kusovníku**.
2. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
    * Můžete vybrat zboží M0055.  
    * Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.  
3. Zaškrtněte políčko položky **Nastavit**.
4. Vyberte možnost *Ano* v poli **Výpočet**.
    * Nastavení vlastností **Výpočet** na hodnotu *Ano* zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.  
5. Vyberte kartu **Nastavení**.
6. Zaškrtněte políčko položky **Nastavit**.
7. Zadejte číslo do pole **Množství**.
    * Pole množství určuje množství zboží, které bude zahrnuto v kusovníku. Může se jednat o zřejmého uchazeče pro mapování atributů.  
8. Vyberte karu **Dimenze**.
    * Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.  
9. Vyberte **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]