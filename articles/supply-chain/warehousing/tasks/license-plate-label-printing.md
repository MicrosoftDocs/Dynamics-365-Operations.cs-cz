---
title: Povolení tisku popisku registrační značky
description: Tohle téma popisuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424170"
---
# <a name="enable-license-plate-label-printing"></a>Povolení tisku popisku registrační značky

[!include [banner](../../includes/banner.md)]

Tohle téma popisuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje. Tento postup můžete projít v ukázkových datech společnosti USMF. Pokud jej používáte s použitím vlastních dat, je třeba mít k nastavenou číselnou řadu pro registračních značky vozidla. Je nutné nastavit tiskárnu štítků před zahájením této úlohy. Přejděte do nabídky Správa organizace > Nastavení > Jednotky Síťové tiskárny. V podokně akcí klikněte na Možnosti a poté klepněte na tlačítko Stáhnout instalační program agenta směrování dokumentů. Spusťte instalační program a ujistěte se, že máte nastavenu síťovou tiskárnu na hodnotu Aktivní předtím, než budete pokračovat v postupu.


## <a name="set-up-the-gs1-company-prefix"></a>Nastavení předpony společnosti GS1
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Parametry řízení skladu**.
2. Do pole **Předpona společnosti GS1** zadejte 7 čísel pro vaše číslo společnosti GS1.
3. Zvolte **Uložit**.
4. Zavřete stránku.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Nastavení číselné řady registrační značky vozidla SSCC
1. Přejděte na **Navigační podokno > Moduly > Správa organizace > Číselné řady > Číselné řady**.
2. Vyberte volbu v poli **Oblast**.
3. Vyberte volbu v poli **Odkaz**.
4. Zadejte hodnotu do pole **Společnost**.
5. Rozbalte sekci **Segmenty**.
6. Vyberte možnost **Upravit**.
7. V tabulce **Segmenty** vyberte první řádek.
8. Vyberte možnost **Odebrat**.
9. Vyberte možnost **Odebrat**.
10. Zvolte **Uložit**.
11. Zavřete stránku.

## <a name="create-the-document-route-layout"></a>Vytvoření rozvržení směrování dokumentu
1. Přejděte do **navigačního podokna > Moduly > Správa skladu > Nastavení > Směrování dokumentu > Rozložení směrování dokumentů**. Povolte rozvržení SSCC.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **ID rozvržení**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte **Vložit na konci textu**.
6. Zvolte **Uložit**.
7. Zavřete stránku.

## <a name="set-up-the-document-routing"></a>Nastavení směrování dokumentu
1. Přejděte do **navigačního podokna > Moduly > Správa skladu > Nastavení > Směrování dokumentu > Směrování dokumentů**.
2. V poli **Typ pracovního příkazu** vyberte možnost.
3. Zvolte **Nové**.
4. Zadejte hodnotu do pole **Sklad**.
5. Zadejte hodnotu do pole **Název**.
6. Zvolte **Nové**.
7. V poli **ID rozvržení** zadejte nebo vyberte hodnotu.
8. V poli **Název** zadejte název tiskárny, kterou chcete použít.
9. Zvolte **Uložit**.
10. Zavřete stránku.

## <a name="create-mobile-device-menu"></a>Vytvoření nabídky mobilního zařízení
1. V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení**.
2. Zvolte **Nové**.
3. Do pole **Název položky nabídky** zadejte hodnotu.
4. Zadejte hodnotu do pole **Nadpis**.
5. V poli **Režim** vyberte režim.
6. V poli **Použít stávající práci** vyberte možnost **Ano**.
7. V poli **Generovat registrační značku** vyberte možnost **Ano**.
8. Rozbalte sekci **Pracovní třídy**.
9. Zvolte **Nové**.
10. Do pole **ID pracovní třídy** zadejte hodnotu.
11. Zvolte **Uložit**.
12. Zavřete stránku.
13. V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení**.
14. Ve stromové struktuře vyberte dříve vytvořenou položku nabídky.
15. Vyberte možnost **Upravit**.
16. Výběrem šipky přidáte do nabídky danou položku.
17. Zvolte **Uložit**.
18. Zavřete stránku.

## <a name="update-a-work-template"></a>Aktualizace šablony práce
1. V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Práce > Pracovní šablony**.
2. Vyberte možnost **Upravit**.
3. Zvolte **Nové**.
4. V poli **Typ práce** vyberte **Tisk**.
5. V poli **ID pracovní třídy** zadejte nebo vyberte hodnotu.
6. Vyberte **Přesunout nahoru**.
7. Zvolte **Uložit**.
8. Zavřete stránku.

