---
title: Vytvoření rozšířených smluv pro účtování na základě průběhu
description: Toto téma vysvětluje, jak vytvořit projektové smlouvy, aby bylo možné vygenerovat faktury pro odběratele na základě procenta dokončené práce.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282815"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Vytvoření rozšířených smluv pro účtování na základě průběhu
[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit projektové smlouvy, aby bylo možné tvořit faktury pro odběratele na základě procenta dokončené práce. Fakturované částky se počítají automaticky pro rozpočtové kategorie práce, které jste nastavili pro projekt. Načasování faktur se nastavuje při vyjednávání projektové smlouvy s odběratelem.

Postupy v tomto tématu slouží k nastavení smlouvy, souvisejícího projektu a pravidel účtování pro výpočet fakturovaných částek pro rozpočtové kategorie práce, které jste nastavili pro projekt.

Po vytvoření smlouvy a projektu můžete nastavit podrobnosti o projektu. Můžete například definovat aktivity a přiřadit zaměstnance do projektu.

## <a name="example"></a>Příklad

Vaše organizace se zabývá vývojem softwaru. Souhlasíte s tím, že pro zákazníka vyvinete balíček pro mzdové účetnictví za celkový poplatek 20 000 USD. Vaše organizace souhlasila s fakturací zákazníka vždy po dokončení určité procentuální části práce na projektu. Pro práci nastavíte následující kategorie projektu, aby je bylo možné použít v procesu fakturace:

- Konzultace
- Návrh
- Instalace

Můžete také nastavit pravidla účtování, která automaticky vypočítají částky faktur pro procentuální část práce projektu dokončenou v každé kategorii.

Správce rozpočtu vytvoří rozpočet pro kategorie projektu. Množství dokončené práce se vypočítá automaticky jako procentuální hodnota dokončené práce z množství práce v rozpočtu.

## <a name="prerequisites"></a>Předpoklady

Před vytvořením projektu, který používá pravidla účtování, je nutné nastavit číselné řady pro pravidla účtování a deník poplatků, který se použije pro zaúčtování vyúčtování postupu.

1. Přejděte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
2. Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Číselné řady** nastavte číselnou řadu, kterou chcete použít při vytváření pravidel účtování.
3. Přejděte na **Řízení a účetnictví projektů** \> **Deníky** \> **Poplatek**.
4. Na stránce **Deník poplatků** vyberte možnost **Nový** a zadejte název deníku.

## <a name="create-a-contract-for-progress-billings"></a>Vytvoření smlouvy pro postupné vyúčtování

Tento postup můžete použít k vytvoření projektové smlouvy pro projekt s pevnou cenou. Fakturu projektu vytvoříte poté, co práce provedená na projektu dosáhne určité procentuální hodnoty.

1. Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Projektové smlouvy**.
2. Na stránce **Projektové smlouvy** zvolte **Nová**.
3. V dialogovém okně **Nová projektová smlouva** nastavte následující pole:

    - **Jméno**
    - **Typ financování**
    - **Zdroj financování**
    - **Měna prodeje** – Ve výchozím nastavení je tato měna používaná pro faktury odběratelů, které jsou přidruženy ke smlouvě projektu. Prodejní měnu však můžete v konkrétní faktuře odběratele upravit.

4. Vyberte **OK**. Informace se zkopírují do záhlaví stránky **Projektových smluv**.
5. Na stránce **Projektové smlouvy** vyplňte zbývající informace o projektu.

## <a name="create-a-project-for-progress-billings"></a>Vytvoření projektu pro postupné vyúčtování

Tyto kroky proveďte k vytvoření projektu a jakýchkoli dílčích projektů spojených s projektovou smlouvou.

1. Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Na stránce **Všechny projekty** zvolte **Nový**.
3. V dialogovém okně **Nový projekt** v poli **Typ projektu** vyberte možnost **Čas a materiál**.
4. Vyberte skupinu projektů. Skupina projektu definuje informace o zaúčtování pro projekty přiřazené ke skupině.
5. Zvolte **Vytvořit projekt**.
6. Po vytvoření projektu nastavte fázi projektu na **Zpracovává se**.

## <a name="create-a-budget-for-a-project"></a>Vytvoření rozpočtu pro projekt

Kategorie rozpočtu slouží k automatickému výpočtu částky faktury za procentuální část práce, která byla dokončena v jednotlivých kategoriích. Chcete-li vytvořit kategorie rozpočtu pro odhadované náklady, postupujte podle následujících kroků.

1. Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Na stránce **Všechny projekty** vyberte a otevřete požadovaný projekt.
3. Na stránce **Projekty** v podokně akcí na kartě **Plán** ve skupině **Rozpočtu** vyberte možnost **Rozpočet projektu**.
4. Na stránce **Rozpočet projektu** zadejte odhadované náklady pro každou kategorii projektu.

## <a name="create-billing-rules-for-progress-billings"></a>Vytvoření fakturačních pravidel pro postupné vyúčtování

1. Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Projektové smlouvy**.
2. Na stránce **Projektové smlouvy** vyberte a otevřete projektovou smlouvu.
3. Na stránce Projektová smlouva na pevné záložce **Pravidla účtování** vyberte **Přidat**.
4. Na stránce **Pravidlo účtování** v poli **Typ řádku** vyberte možnost **Průběh**.
5. Na pevné záložce **Podrobnosti řádku pravidla účtování** zadejte do pole **Hodnota smlouvy** celkovou hodnotu smlouvy.
6. V poli **Kategorie** vyberte kategorii, do které chcete zaúčtovat transakci poplatku.
7. V poli **Projekt** vyberte projekt nebo úkol, který používá toto pravidlo účtování.
8. Vyolitelné: Pravidlo účtování můžete přiřadit dalším projektům. Na pevné záložce **Projekt** v části **Dostupné projekty** vyberte projekt a poté výběrem tlačítka se šipkou vpravo přidejte projekt do oddílu **Vybrané projekty**.
9. Volitelné: Můžete zadat procento k výpočtu částky, kterou odběratel srazí z plateb na faktuře. Na pevné záložce **Podmínky zadržení platby** vyberte zdroj financování a poté v poli **Procento zádržného** zadejte procento zádržného.
10. Opakujte tyto kroky a vytvořte další pravidla účtování pro projektovou smlouvu.
