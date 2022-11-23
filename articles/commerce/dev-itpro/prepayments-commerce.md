---
title: Zálohy v aplikaci Dynamics 365 Commerce
description: Tento článek poskytuje přehled zpracování transakcí záloh v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780351"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Zálohy v aplikaci Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Tento článek poskytuje přehled zpracování transakcí záloh v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce zpracovává zálohy pro následující typy plateb, které se používají v pohledávkách nebo Commerce:

- **Platba zálohy na zákaznický účet** – Zákazník zaplatí zálohu v místě prodeje (POS). Commerce zpracovává zálohovou platbu jako platbu předem. Když zaúčtujete transakci, vytvoří se deník plateb a zaúčtuje se na stránku **Poukaz na deník** v Commerce headquarters. Zaškrtávací políčko **Zálohový doklad deníku** na kartě **Platba** je automaticky vybráno pro deník plateb. Další informace, včetně informací o platbě předem a konkrétních daní, které jsou relevantní pro cílový region, naleznete na adrese [Zdroje globalizace – obsah nápovědy specifický pro zemi/oblast](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Objednávka zákazníka, která má zálohu** – Zákazník vytvoří zákaznickou objednávku na POS. Zákazník může za objednávku zaplatit zálohu na základě výchozího procenta zálohy, které je nakonfigurováno na stránce **Objednávky zákazníků** v Commerce headquarters (**Parametry Commerce \> Objednávky zákazníků**). Commerce zpracovává zálohovou platbu pro objednávku zákazníka jako platbu předem. Když zaúčtujete transakci, vytvoří se deník plateb a zaúčtuje se na stránku **Poukaz na deník**. Zaškrtávací políčko **Zálohový doklad deníku** na kartě **Platba** je automaticky vybráno pro deník plateb. Platba je zúčtována a při vyzvednutí nebo doručení objednávky je automaticky vystavena zákaznická faktura.
- **Prodejní objednávka call centra** – Zástupce zákaznického servisu call centra vytvoří prodejní objednávku jménem zákazníka atribut **platba předem** je nastaven na **Ano** během zachycení platby.

Commerce provádí při zpracování zálohy následující úkoly:

- **Zpracovat platbu zálohy na zákaznický účet** – Záloha, kterou zákazník provede, je převedena do Commerce pomocí služby, která synchronizuje data. Commerce vytvoří maloobchodní platební transakci pro platbu. Když zaúčtujete maloobchodní transakci, zaúčtuje se peněžní deník nebo deník plateb zákazníka. Zaškrtávací políčko **Zálohový doklad deníku** na kartě **Platba** stránky **Doklad deníku** v Commerce headquarters je automaticky vybráno pro deník plateb. Zálohy nelze zpracovat, pokud je částka platby záporná.
- **Zpracovat objednávku zákazníka nebo prodejní objednávku, která má zálohu** – Zákazník zaplatí požadovanou zálohu za zákaznickou objednávku pomocí Commerce Data Exchange: Služba v reálném čase. Commerce vytváří buď zákaznický platební deník, nebo pokladní deník, v závislosti na způsobu platby, který zákazník používá. Zaškrtávací políčko **Zálohový doklad deníku** na kartě **Platba** stránky **Doklad deníku** je automaticky vybráno pro deník plateb v Commerce headquarters. Pokud zákazník používá více způsobů platby k částečným platbám, Commerce zpracuje každou částečnou platbu na základě způsobu platby, který byl použit.

U kreditních karet a u digitálních peněženek, které mají základní platební metody kreditní kartou, Commerce po úspěšné autorizaci odešle žádost o „zachycení“. (Prostředky jsou zachyceny před fakturací prodejní objednávky.)

Pokud zrušíte objednávku zákazníka, částka zálohy bude vrácena a pro částku zálohy bude zveřejněn deník plateb. Vrácená částka je vypočítána a zaúčtována na základě způsobu platby, který jste uvedli při zaúčtování refundační platby. Commerce může účtovat storno poplatek na základě procenta, které nastavíte na stránce **Parametry Commerce** v Commerce headquarters.

Pokud vrátíte objednávku zákazníka, vytvoří se objednávka vrácení a deník plateb vrácení peněz. Když zaúčtujete objednávku vrácení, Commerce vytvoří buď deník plateb zákazníka, nebo peněžní deník, v závislosti na způsobu platby, který zákazník použil pro původní transakci.
