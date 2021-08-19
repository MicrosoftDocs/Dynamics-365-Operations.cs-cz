---
title: Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu
description: Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da52385f60b2522cf358e0ceb70448479a1e5dc714ef15ba361611ed404ed852
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726818"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu. Tato procedura také ukazuje, jak lze vytvářet názvosloví konfigurace komponenty modelu konfigurace produktu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Základnímu produktu D0004 je přiřazeno nové názvosloví čísla produktu. Tento úkol obvykle provádí návrhář produktu.

## <a name="create-a-product-number-nomenclature"></a>Vytvoření názvosloví čísla produktu

1. Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Nomenklatura produktu**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Název**.
1. Zadejte hodnotu do pole **Popis**.
1. Vyberte **přidat**.
1. Zvolte **Číslo základního produktu**.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Označte na seznamu vybraný řádek.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Konfigurace**.
1. Zavřete stránku.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Přiřazení názvosloví čísla produktu základnímu produktu

1. Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.
1. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole **Číslo produktu** pomocí hodnoty „D“.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Vyberte možnost **Upravit**.
1. Vyberte možnost *Ano* v poli **Použít názvosloví**.
1. V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.
1. Zavřete stránku.
1. Zavřete stránku.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Vytvoření názvosloví pro komponentu modelu konfigurace produktu

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Vyberte možnost **Upravit**.
1. Vyberte možnost *Ano* v poli **Použít konfiguraci**.
1. Vyberte **přidat**.
1. Vyberte **Hodnota atributu**.
1. Označte na seznamu vybraný řádek.
1. V poli **Atribut** zadejte nebo vyberte hodnotu.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Označte na seznamu vybraný řádek.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Hodnota atributu**.
1. Označte na seznamu vybraný řádek.
1. V poli **Atribut** zadejte nebo vyberte hodnotu.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Označte na seznamu vybraný řádek.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Hodnota atributu**.
1. Označte na seznamu vybraný řádek.
1. V poli **Atribut** zadejte nebo vyberte hodnotu.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Označte na seznamu vybraný řádek.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Hodnota atributu**.
1. Označte na seznamu vybraný řádek.
1. V poli **Atribut** zadejte nebo vyberte hodnotu.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Označte na seznamu vybraný řádek.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Hodnota číselné řady**.
1. Označte na seznamu vybraný řádek.
1. V poli **Číselná řada** zadejte nebo vyberte hodnotu.
1. Zavřete stránku.
1. Zavřete stránku.
1. Zavřete stránku.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]