---
title: Příprava pro ostré nasazení Human Resources
description: Tato stránka poskytuje pokyny, jak se připravit na uvedení do provozu Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2020
ms.locfileid: "4417707"
---
# <a name="prepare-for-human-resources-go-live"></a>Příprava pro ostré nasazení Human Resources

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak se připravit na uvedení do provozu projektu Dynamics 365 Human Resources pomocí Microsoft Dynamics Lifecycle Services (LCS). 

Tato grafika ukazuje fáze procesu uvedení do provozu. 

![Proces ostrého nasazení](./media/hr-admin-go-live-prepare-process.png)

V následující tabulce jsou uvedeny všechny kroky v procesu, očekávané trvání a kdo je za akci odpovědný.

| Fáze | Akce | Doba trvání / kdy | Kdo | Poznámky |
| --- | --- | --- | --- |--- |
| 1 | Aktualizujte datum uvedení do provozu v LCS | Nejpozději 2-3 měsíce předem | Partner / zákazník | Data milníku by měla být průběžně aktualizována. |
| 2 | Vyplňte a odešlete kontrolní seznam | Po doknčení uživatelského akceptačního testování (UAT) | Partner / zákazník | Postupujte podle pokynů uvedených v [Vyhodnocení funkce FastTrack naživo](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Hodnocení projektu (FastTrack) | FastTrack Architect * | Architekt poskytuje posouzení po obdržení kontrolního seznamu a pokračuje v kontrole, dokud nejsou vyjasněny otázky a pokud nejsou k dispozici zmírnění. |
| 4 | Projektový workshop (FastTrack) | FastTrack Architect * | |
| 5 | Import datového balíčku | Závisí na projektu | Partner / zákazník | Postupujte podle pokynů v [Přehledu správy dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Připraveno na produkci | Po dokončení všech předchozích kroků | Partner / zákazník | Partner / zákazník může převzít kontrolu nad produkčním prostředím.|
| 7 | Činnosti přechodu | Závisí na projektu | Partner / zákazník | |
| 8 | Přechod do ostrého nasazení | Závisí na projektu | Odběratel | |

> [!IMPORTANT]
> *Kroky 3 a 4 jsou dokončeny pouze pro zákazníky, kteří mají nárok na FastTrack.

## <a name="completing-the-lcs-methodology"></a>Dokončení metodiky LCS

Hlavním milníkem v každém implementačním projektu je přechod do produkčního prostředí. 

Abychom zajistili, že se produkční prostředí používá pro živé operace, Microsoft zřídí produkční instanci pouze v případě, že se implementace blíží do fáze **Provoz** po dokončení požadovaných činností v metodice LCS. Další informace o prostředích ve vašem předplatném najdete v části  [Průvodce licencováním Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544). 

Zákazníci musí dokončit fáze **Analýza**, **Design a vývoj** a **Test** v metodice LCS před tím, než je k dispozici tlačítko **Konfigurovat**  pro vyžádání produkčního prostředí. Chcete-li dokončit fázi v LCS, musíte nejprve dokončit všechny požadované kroky v této fázi. Když jsou dokončeny všechny kroky ve fázi, můžete dokončit celou fázi. Fázi můžete kdykoli znovu otevřít, pokud musíte provést změny. Další informace viz  [Lifecycle Services (LCS) pro zákazníky aplikací Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Proces dokončení kroku má dvě části: 

- Proveďte skutečnou práci, jako je analýza přizpůsobení a mezer nebo testování přijetí uživatele (UAT). 
- Označte odpovídající krok v metodice LCS jako dokončený. 

Dobrou praxí je plnění kroků v metodice při postupu v implementaci. Nečekejte až na poslední chvíli. Neklikejte jen na všechny kroky, abyste získali produkční prostředí. Je v nejlepším zájmu zákazníka mít solidní implementaci. 

## <a name="uat-for-your-solution"></a>UAT pro vaše řešení

Během fáze UAT musíte otestovat všechny obchodní procesy, které jste implementovali, a veškerá přizpůsobení, která jste provedli, v prostředí Sandbox v implementačním projektu. Abychom vám pomohli zajistit úspěšné uvedení do provozu, měli byste při dokončení fáze UAT zvážit následující: 

- Testovací případy pokrývají celý rozsah požadavků. 
- Otestujte pomocí migrovaných dat. Tato data by měla zahrnovat kmenová data, jako jsou pracovníci, úlohy a pozice. Zahrňte také počáteční zůstatky, jako je nahromadění dovolené a absence. Nakonec zahrňte otevřené transakce, jako jsou aktuální registrace výhod. Kompletní testování se všemi typy dat, i když datová sada není dokončena. 
- Testujte pomocí správných rolí zabezpečení (výchozí role a vlastní role), které jsou přiřazeny uživatelům. 
- Ujistěte se, že řešení splňuje veškeré regulační požadavky specifické pro společnost a odvětví. 
- Zdokumentujte všechny funkce a získejte souhlas a potvrzení od zákazníka. 

## <a name="fasttrack-go-live-assessment"></a>Test naživo FastTrack

Zákazníci, kteří mají kvalifikaci pro FastTrack a jsou zapojeni do FastTrack Solution Architect, dokončí hodnocení přechodu do ostrého provozu s Microsoft FastTrack. Další informace viz  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Asi osm týdnů před uvedením do provozu vás tým FastTrack požádá o vyplnění [Kontrolního seznamu pro přechod od ostrého provozu](https://go.microsoft.com/fwlink/?linkid=2146013).

Manažer projektu nebo klíčový člen projektu musí během kontrolní fáze před zahájením projektu vyplnit kontrolní seznam uvedení do provozu. Kontrolní seznam je obvykle dokončen čtyři až šest týdnů před navrhovaným datem uvedení do provozu, kdy je UAT dokončen nebo téměř dokončen. 

Po dokončení kontrolního seznamu jej odešlete e-mailem svému architektovi řešení FastTrack. Na e-mail vždy uveďte klíčovou zúčastněnou stranu od zákazníka a implementačního partnera. 

Po odeslání kontrolního seznamu váš architekt řešení FastTrack zkontroluje projekt a poskytne posouzení, které popisuje potenciální rizika, osvědčené postupy a doporučení pro úspěšné uvedení projektu do provozu. V některých případech může architekt řešení upozornit na rizikové faktory a požádat o plán zmírnění. 

## <a name="see-also"></a>Viz také

[Často kladené dotazy týkající se ostrého nasazení](hr-admin-go-live-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]