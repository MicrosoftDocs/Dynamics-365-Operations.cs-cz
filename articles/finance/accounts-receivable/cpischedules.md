---
title: Plán indexu spotřebitelských cen
description: Tento článek vysvětluje, jak vytvořit seznam plánů indexu spotřebitelských cen (CPI), který získáte z internetu, abyste mohli určit eskalační poplatek ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904866"
---
# <a name="consumer-price-index-schedule"></a>Plán indexu spotřebitelských cen

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit, odstranit, zkontrolovat a zpracovat plány indexu spotřebitelských cen (CPI). Plán CPI lze použít k určení cen spotřebního zboží a služeb, které přidáte jako řádky plánu fakturace. Rozvrh CPI pak lze použít s eskalačními a diskontními cenami ve fakturačním rozvrhu, nebo jej lze ručně zpracovat za účelem aktualizace fakturačních částek ve fakturačních rozvrhech. Plány CPI můžete zadat ručně nebo je můžete importovat pomocí složené entity plán CPI.

Chcete-li přidat plán CPI, postupujte takto:

1. Na stránce **Plán indexu spotřebitelských cen** vyberte položku **Nový**.
2. V poli **Plán indexu spotřebitelských cen** zadejte jedinečný název.
3. Zadejte popis do pole **Popis**.
4. Na kartě **Plán indexu spotřebitelských cen** vyberte položku **Přidat**.
5. V poli **Datum indexu spotřebitelských cen** zadejte datum, kdy bude nový plán CPI aktivní.
6. V poli **Plán indexu spotřebitelských cen** zadejte název, který jste zadali v kroku 2.
7. Zvolte možnost **Uložit**.

Při odstraňování data plánu CPI postupujte takto:

1. Na stránce **Plán indexu spotřebitelských cen** vyberte jeden nebo více řádků, které chcete odstranit, a poté vyberte **Odstranit**.
2. Chcete-li odstranit celý plán CPI, v podokně akcí vyberte **Vymazat**. Vybraný plán CPI nelze smazat, pokud je spojen s jakýmkoli plánem fakturace.
3. V podokně akcí vyberte **Proces** k aktualizaci rozvrhů fakturace, které používají vybraný rozvrh CPI. Nejnovější data CPI a částky plánu budou použity k aktualizaci cen plánu fakturace.
4. Na pevné záložce **Proces indexu spotřebitelských cen** zkontrolujte aktualizovaná pole **Číslo fakturačního plánu**, **Číslo položky**, **Datum zahájení fakturace**, **Datum ukončení fakturace**, **Datum eskalace** a **Frekvence eskalace**.

Poté, co jsou plány CPI nastaveny, lze je použít pro eskalaci a změny cen ve fakturačních plánech.

## <a name="cpi-calculation"></a>Výpočet CPI

Pro tyto příklady je období od 1. ledna 2020 do 31. prosince 2022. Základní sazba CPI (hodnota CPI při zahájení smlouvy) je 105,65. K 1. lednu 2021 je aktuální CPI 110,5. K 1. lednu 2022 je aktuální CPI 114,25. Počáteční částka je 1000.

**Příklad 1**

Na stránce **Parametry opakované fakturace smlouvy**, nastavíte pole **Výpočet indexu spotřebitelských cen** na **Základní index spotřebitelských cen**.

Pro období 1. ledna 2021 se první částka eskalace vypočítává následujícím způsobem na základě počáteční částky:

1000 + (110,5 - 105,65) &divide; 105.65 &times; 1000 = 1045,91

Pro období 1. ledna 2022 se částka eskalace vypočítává následujícím způsobem:

1000 + (114,25 - 105,65) &divide; 105,65 &times; 1000 = 1081,40

**Příklad 2**

Na stránce **Parametry opakované fakturace smlouvy**, nastavíte pole **Výpočet indexu spotřebitelských cen** na **Předchozí index spotřebitelských cen**.

Pro období 1. ledna 2021 se první částka eskalace vypočítává následujícím způsobem na základě počáteční částky:

1000 + (110,5 - 105,65) &divide; 105.65 &times; 1000 = 1045,91

Pro období 1. ledna 2022 se částka eskalace vypočítává následujícím způsobem na základě první částky eskalace:

1045,91 + (114,25 - 110,5) &divide; 110,5 &times; 1045,91 = 1081,40

> [!NOTE]
> Proces eskalace vždy používá nejnovější hodnotu CPI bez ohledu na datum indexu. Pokud je například eskalace v září, ale poslední hodnota CPI je pro červenec, použije se červencový index. Po zadání zářijového indexu se neprovádějí žádné úpravy.

## <a name="prorated-escalation"></a>Poměrná eskalace

Pokud k eskalaci dojde uprostřed zúčtovacího období, částka je poměrná. Fakturační období je například od 1. srpna 2020 do 31. července 2021. K datu CPI 1. září 2019 je hodnota CPI 244. K datu CPI 1. září 2020 je hodnota CPI 250. Pokud je předchozí sazba 1 000, použijí se pro výpočet fakturační částky za období následující vzorce:

* *Změny CPI* = (250 – 244) &divide; 244 = 2,459%
* *Aktuální sazba* = 1000 &times; 2,459% = 1024,59
* *Počet dní za aktuální sazbu* = 31. července 2021 – 1. září 2020 = 334
* *Předchozí sazba* = 1 000
* *Počet dní za předchozí sazbu* = 31. srpna 2020 – 1. srpna 2020 = 31
* *Celkový počet dní ve fakturačním období* = 31. července 2021 – 1. srpna 2020 + 1 = 365
* *Fakturační částka za toto období* = (1000 &times; 31 &divide; 365) + (1 024,59 &times; 334 &divide; 365) = 1 022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalace, která používá CPI a procento

Eskalace lze provádět pomocí CPI. CPI plus 3procentní eskalace začíná 1. ledna 2020 a má roční frekvenci.

- Částka, která je fakturována od 1. ledna 2019 do 31. prosince 2020, je 4 000.
- Fakturační období, které bude eskalováno, je od 1. ledna 2020 do 31. prosince 2020.
- K datu CPI 1. prosince 2018 je hodnota CPI 205,3. K datu CPI 1. prosince 2019 je hodnota CPI 219,6.

Pokud je předchozí sazba 4 000, fakturační částka za období se vypočítá následovně:

- *Změny CPI* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Aktuální sazba* = (4000 &times; 6,965%) - 4000 = 278,60
- *Procentuální změny* = (4000 &times; 1,03) – 4000 = 120
- *Fakturační částka* = 4000 + 278,6 + 120 = 4398,6
