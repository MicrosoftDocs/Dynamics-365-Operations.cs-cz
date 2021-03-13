---
title: Země/oblast původu
description: Mnoho organizací vydává certifikáty svým dodavatelům, aby zajistily, že produkty splňují specifické certifikační standardy. Tyto certifikáty často závisí na zemi původu. Toto téma obsahuje informace o funkci země původu, která vám umožňuje propojit produkt s jeho zemí původu a sledovat jeho certifikace produktu.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2eaf0057123cd2cbcad00f95038627291dada517
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007801"
---
# <a name="country-of-origin"></a>Země/oblast původu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mnoho organizací vydává certifikáty svým dodavatelům, aby zajistily, že produkty splňují specifické certifikační standardy. Tyto certifikáty často závisí na zemi původu. Funkce země původu, která vám umožňuje propojit produkt s jeho zemí původu a sledovat jeho certifikace produktu.

## <a name="turn-on-the-country-of-origin-feature"></a>Zapnutí funkci země původu

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul**: *Řízení informací o produktech*
- **Název funkce:** *Funkce správy země původu*

## <a name="configure-source-and-destination-countries"></a>Nakonfigurujte zdrojové a cílové země

Před vydáním certifikátu pro produkt musíte produkt propojit s cílovou zemí a zemí původu.

1. Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Pravidla země původu**.
2. Vyberte existující nastavení země, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení země.
3. Nastavte následující hodnoty pro vybranou nebo novou zemi.

    | Pole | popis |
    |---|---|
    | Č. položky | Vyberte číslo položky produktu. |
    | Cílová země | Vyberte zemi, do které odesíláte produkt. |
    | Země původu | Vyberte zemi, ze které odesíláte produkt. |

Účelem tohoto nastavení je pomoci vám vygenerovat sestavu kusovníku (BOM), kde můžete zahrnout zemi původu pro každou část, pro kterou jsou zdrojové a cílové země určeny. Tato zpráva vám pomůže získat ucelený obrázek o tom, odkud vaše součásti pocházejí a kam směřují.

## <a name="keep-track-of-vendor-certificates"></a>Sledujte certifikáty dodavatelů

Můžete použít stránku **Osvědčení prodejců země původu** pro sledování certifikátů, které vydáváte prodejcům.

Musíte se rozhodnout, které certifikáty vydáváte a jakým způsobem je budete hlásit zákazníkům. Tato funkce pomáhá sledovat vaše certifikáty. Umožňuje také zvolit, zda se příslušná čísla certifikátů budou zobrazovat na fakturách, dodacích listech nebo potvrzeních objednávek.

Chcete-li nastavit informace certifikátů, postupujte následujícím způsobem.

1. Přejděte na **Správa informací o produktu \> Založit \> Shoda výrobků \> Země původu \> Certifikáty dodavatelů země původu**.
2. Vyberte existující nastavení certifikátu, které chcete upravit, nebo vyberte **Nový** v podokně akcí a vytvořte nové nastavení certifikátu.
3. Proveďte následující nastavení pro vybraný nebo nový certifikát.

    | Pole | popis |
    |---|---|
    | Účet dodavatele | Vyberte dodavatele, kterému jste certifikát vydali. |
    | Č. položky | Vyberte položku, které jste certifikát vydali. |
    | Země / oblast | Cílová země nebo region, kde musíte tento certifikát použít. |
    | Číslo certifikátu | Zadejte identifikační číslo certifikátu, který jste vydali. |
    | Platný | Vyberte první datum, kdy je aktuální certifikát platný.|
    | Vypršení platnosti | Vyberte poslední datum, kdy je aktuální certifikát platný. |
    | Vytisknout na fakturu | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na fakturách, které jsou adresovány konkrétní zemi během zadaného časového období. |
    | Vytisknout na dodacím listu | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na dodacích listech, které jsou adresovány konkrétní zemi během zadaného časového období. |
    | Vytisknout na prodejní objednávku | Zaškrtněte toto políčko, chcete-li vytisknout číslo certifikátu na prodejních objednávkách, které jsou adresovány konkrétní zemi během zadaného časového období. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Uveďte zemi původu do hlášení kusovníku

Při generování sestavy kusovníku můžete pro každou část, pro kterou jste určili zdrojovou a cílovou zemi, zadat zemi původu na stránce **Pravidla země původu**.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte nebo vytvořte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.
1. V podokně akcí na kartě **Analyzovat** ve skupině **BOM** zvolte **Návrhář**.
1. Na stránce, která se zobrazí, v podokně akcí vyberte **BOM \> Tisk**.
1. V dialogovém okně **Řádky kusovníku** nastavte pole **Cílová země** na cílovou zemi, kterou chcete zobrazit v sestavě.
1. Vyberte **OK**.

Je vygenerována a zobrazena sestava, která zobrazuje informace o zemi původu každé části. Následuje příklad sestavy.

![Sestava země původu](media/country-of-origin-report.png "Sestava země původu")
