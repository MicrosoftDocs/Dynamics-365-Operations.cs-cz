---
title: Nastavení a používání plateb dodavatelům způsobem „zaplatit při uhrazení“
description: Toto téma vysvětluje, jak vytvořit podmínky platby po zaplacení (ZPZ) tak, aby bylo možné uvolnit částečné platby dodavatelů na základě plateb odběratelů.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284106"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Nastavení a používání plateb dodavatelům způsobem „zaplatit při uhrazení“

[!include [banner](../includes/banner.md)]

Po schválení dodavatele jako subdodavatele lze zadržet platby dodavateli, dokud nebudete odběratelem zaplaceni za projekt. Chcete-li podporovat tento scénář, nastavte podmínky platby po zaplacení (ZPZ) při nastavení nákupní objednávky (PO) u dodavatele.

Například když odběratel zaplatí částku uvedenou na faktuře projektu, můžete uvolnit část nebo celou částku faktury dodavatele. Prostě nastavte podmínky ZPZ, které určí, že dodavatel bude vyplacen poté, co obdržíte poměrnou část související platby od odběratele. Když obdržíte částečnou platbu obdržíte od odběratele, můžete některé související faktury dodavatele k platbě vydat ručně.

Následující příklad popisuje proces, kdy jsou použity podmínky ZPZ.

## <a name="example"></a>Příklad

Vaše organizace souhlasí s tím, že poskytne zákazníkovi 100 počítače s nainstalovaným softwarem za cenu 150,00 USD pro každý počítač. Poté přiřadíte dodavatele, který vám poskytne počítače, ve kterých je nainstalován software. Podle smlouvy musí zákazník schválit kvalitu počítačů předtím, než zaplatí organizaci. Zásady vaší organizace odpírá platbu dodavatelům, dokud vám jej odběratel nezaplatí. Projekt tedy nastavíte tak, aby ZPZ procento bylo 100 procent.

Dodavatel vám pošle 100 počítačů, které mají nainstalovaný software, spolu s fakturou na 10 000,00 USD. Vzhledem k tomu, jak jsou nastaveny ZPZ podmínky pro váš projekt, neplatíte dodavateli po obdržení počítačů. Namísto toho odešlete počítače odběrateli spolu s fakturou na 15 000,00. Odběratel počítače zkontroluje a schválí plnou částku projektové faktury.

Poté, co obdržíte celou platbu od odběratele, můžete zaplatit dodavateli celou částku faktury dodavatele, 10 000,00.

## <a name="set-up-pwp-terms-for-a-project"></a>Nastavení podmínek ZPZ pro projekt

Když pro projekt nastavíte podmínky ZPZ, je nutné zadat jako procento minimální částku, kterou musí odběratel uhradit za projekt před tím, než zaplatíte dodavateli. Prahové množství je automaticky přepočítáno na faktuře odběratele pro projekt. Chcete-li nastavit prahová procenta pro podmínky ZPZ, postupujte takto:

1. Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Vyhledejte a otevřete projekt, pro který chcete vytvořit ZPZ podmínky.
3. Na pevné kartě **Smlouvy s dodavatelem** vyberte tlačítko **Přidat řádek**.
3. V poli **Kód účtu** vyberte jednu z následujících možností:

    - **Tabulka** – Podmínky ZPZ platné pro jednoho dodavatele.
    - **Skupina** – Podmínky ZPZ platné pro všechny dodavatele ve skupině dodavatelů.
    - **Vše** – Podmínky ZPZ platné pro všechny dodavatele.

4. Pokud jste v předchozím kroku vybrali **Tabulka** nebo **Skupina** v poli **Dodavatel/Skupina dodavatelů**, vyberte dodavatele nebo skupinu dodavadelů, na které se podmínky ZPZ vztahují. Pokud jste v předchozím kroku vybrali **Vše** pole **Dodavatel/Skupina dodavatelů** nebude možné upravit.
5. Pokud jsou v projektu nastaveny také podmínky uchovávání informací dodavatele, v poli **Podmínky zádržného dodavatele** vyberte ID pravidla pro podmínky uchovávání.
6. V poli **Procento prahu ZPZ** zadejte procentuální mezní hodnotu pro projekt. Procento, které jste zadali pro projekt, definuje minimální částku, kterou vám odběratel musí zaplatit předtím, než zaplatíte dodavateli.

## <a name="create-a-po-that-has-pwp-terms"></a>Vytvořit objednávku, která má ZPZ podmínky

Pokud zaúčtujete faktury od dodavatele a dodavatel se řídí podmínkami ZPZ, tyto podmínky jsou zobrazeny v řádcích nákupní objednávky. Chcete-li vytvořit nákupní objednávku, která má ZPZ podmínky, postupujte podle následujících kroků.

1. Přejděte na **Zásobování a zdroje** \> **Nákupní objednávky** \> **Všechny nákupní objednávky**.
2. V podokně akcí zvolte **Nový**. Poté v dialogovém okně **Vytvořit nákupní objednávku** zadejte požadované informace a vyberte **OK**.

    Další možností je otevření existující nákupní objednávky na stránce se seznamem **Všech nákupních objednávek**.

4. Na stránce **Nákupní objednávka** na pevné záložce **Řádky nákupní objednávky** zkontrolujte podrobnosti řádku nákupní objednávky pro dodavatele. Je automaticky vybrána možnost **Zaplatit po zaplacení** a hodnota v poli **Procento prahu ZPZ** je automaticky zkopírována z pole **Procento prahu ZPZ** na stránce **Projekty**.
6. Nechcete-li pro řádek nákupní objednávky použít podmínky ZPZ, zrušte zaškrtnutí možnosti **zaplatit po zaplacení.** V tomto případě bude **Procento prahu ZPZ** pro řádek nákupní objednávky vynulováno na hodnotu 0 (nula).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu odběratele a proveďte úhradu dodavateli

Jakmile dodavatel dokončí práci na projektu a vy obdržíte fakturu, musíte zkontrolovat stav projektu a fakturu odběratele a ověřit, zda byly u projektu splněny podmínky ZPZ. Pokud byly splněny podmínky ZPZ dodavatele, můžete na základě plateb odběratele za projekt určit, které řádky na faktuře dodavatele uhradit. Pokud se rozhodnete zaplatit dodavatele i přesto, že ZPZ podmínky nebyly splněny, můžete přepsat ZPZ podmínky na stránce **Faktury dodavatele s platbou po zaplacení**.

1. Přejděte na **Řízení projektů a účetnictví** \> **Dotazy a sestavy** \> **Dotazy na zadržení** \> **Faktury dodavatele s platbou po zaplacení**.
2. Na stránce **Faktury dodavatele s platbou po zaplacení** zadejte do pole Hledat hodnoty, pro které chcete najít fakturu dodavatele, kterou chcete zkontrolovat, a poté vyberte **Hledat**.
3. Na záložce **Řádky faktury dodavatele** vyberte řádky, které chcete změnit.
4. Pokud jsou splněny podmínky **Zaplatit po zaplacení** pro řádek faktury, vyberte **Uvolnit platbu dodavatele**. Označení možnosti **Zaplatit po zaplacení** je zrušeno a hodnota pole **Připraveno k platbě** se změní na **Ano**.
