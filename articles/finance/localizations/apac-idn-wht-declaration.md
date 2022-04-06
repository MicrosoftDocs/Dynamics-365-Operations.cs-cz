---
title: Výkaz srážkové daně pro Indonésii
description: Toto téma vysvětluje, jak nakonfigurovat a vygenerovat výkaz srážkové daně pro Indonésii.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943654"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Výkaz srážkové daně pro Indonésii (ID-00005)

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit a vygenerovat soubor srážkové daně PPH, který právnické osoby v Indonésii používají k vykazování srážkové daně v aplikaci e-Bupot.

Indonéský daňový úřad (DGT) stanovuje, že podnikatelé povinní k dani (PKP), kteří jsou registrováni u KPP Pratama jako osoby oprávněné ke srážce daní / výběru daně z příjmu (PPh) podle článku 23 a/nebo článku 26, musí elektronicky podávat přiznání k dani z příjmu podle článku 23 a 26 pomocí aplikace e-Bupot. 

- **Článek 23** – Výkaz obsahuje všechny srážkové transakce od dodavatelů, u nichž je kód země/oblasti primární adresy kódem pro Indonésii.
- **Článek 26** – Výkaz obsahuje všechny srážkové transakce od dodavatelů, u nichž není kód země/oblasti primární adresy kódem pro Indonésii.

## <a name="prerequisites"></a>Předpoklady

- Primární adresa právnické osoby musí být v Indonésii.
- V pracovním prostoru **Správa funkcí** musí být zapnuta funkce **Globální srážková daň**. Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Stažení konfigurací elektronického výkaznictví

Generování souboru importu je založeno na konfiguracích elektronického vykazování. Další informace o možnostech a konceptech konfigurovatelných sestav najdete v tématu [Elektronické přiznání](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Prostředí provozního a uživatelského akceptačního testování (UAT) najdete v pokynech v tématu [Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Chcete-li vygenerovat soubor importu, nahrajte z úložiště následující konfigurace:

- **Model daňového přiznání.verze.93.xml** nebo novější
- **Mapování modelu daňového přiznání.verze.93.153.xml** nebo novější
- **Import schématu PPh srážkové daně (ID).verze.93.14** nebo novější

## <a name="set-up-general-ledger-parameters"></a>Nastavení parametrů hlavní knihy

1. Přejděte na **Daň** \> **Nastavení** \> **Parametry hlavní knihy**.
2. Na kartě **Srážková daň** v poli **Mapování formátu přiznání ke srážkové dani** vyberte **Import schématu PPh srážkové daně (ID)**. 
3. Jděte na **Daň** \> **Nastavení** \> **Srážková daň** \> **Typy výnosů srážkové daně**, kde nastavte typ výnosu srážkové daně **Kode Bukti Potong** a poté přiřaďte kódy ke skupinám srážkové daně související položky. Kódy jsou nutné pro vygenerování integračního souboru pomocí aplikace e-Bupot. 

## <a name="generate-the-withholding-import-file"></a>Generování souboru importu srážkové daně

Proces přípravy a generování souboru e-Bupot pro konkrétní období je založen na transakcích srážkové daně zaúčtovaných během úlohy vypořádání nebo platby daně.

Při generování souboru postupujte následovně.

1. Jděte na **Daň** \> **Přiznání** \> **Srážková daň** \> **Import souboru PPH e-bupot 23 a 26**.
2. Pro výkaz vyberte datum „od“ a „do“ a vyberte období vyrovnání.
3. Zadejte datum transakce a poté vyberte **OK**.
4. Vyberte jazyk. Všechny výkazy jsou přeloženy do americké angličtiny (**en-us**) a indonéštiny (**id**).
5. Vyberte typ podniku a poté zadejte číslo šeku a dokladu. 
6. Zkontrolujte, zda byl výkaz podepsán manažerem. Tyto informace budou vykázány v souboru. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]