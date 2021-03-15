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
ms.openlocfilehash: b4196532be8ad40bacb8d614c6b0c86215b00bdb
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111737"
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

Hlavním milníkem v každém implementačním projektu je přechod do produkčního prostředí. Proces dokončení kroku má dvě části: 

- Proveďte skutečnou práci, jako je analýza přizpůsobení a mezer nebo testování přijetí uživatele (UAT). 
- Označte odpovídající krok v metodice LCS jako dokončený. 

Dobrou praxí je plnění kroků v metodice při postupu v implementaci. Nečekejte až na poslední chvíli. Je v nejlepším zájmu zákazníka mít solidní implementaci. 

## <a name="uat-for-your-solution"></a>UAT pro vaše řešení

Během fáze UAT musíte otestovat všechny obchodní procesy, které jste implementovali, a veškerá přizpůsobení, která jste provedli, v prostředí Sandbox v implementačním projektu. Abychom vám pomohli zajistit úspěšné uvedení do provozu, měli byste při dokončení fáze UAT zvážit následující: 

- Doporučujeme, aby váš proces UAT začínal čistým a čerstvým prostředím, kde jsou data z vaší konfigurace GOLD zkopírována do prostředí před spuštěním procesu UAT. Jako prostředí GOLD doporučujeme používat provozní prostředí, dokud nebude v ostrém provozu, kdy se prostředí stává provozním.
- Testovací případy pokrývají celý rozsah požadavků. 
- Otestujte pomocí migrovaných dat. Tato data by měla zahrnovat kmenová data, jako jsou pracovníci, úlohy a pozice. Zahrňte také počáteční zůstatky, jako je nahromadění dovolené a absence. Nakonec zahrňte otevřené transakce, jako jsou aktuální registrace výhod. Kompletní testování se všemi typy dat, i když datová sada není dokončena. 
- Testujte pomocí správných rolí zabezpečení (výchozí role a vlastní role), které jsou přiřazeny uživatelům. 
- Ujistěte se, že řešení splňuje veškeré regulační požadavky specifické pro společnost a odvětví. 
- Zdokumentujte všechny funkce a získejte souhlas a potvrzení od zákazníka. 

## <a name="mock-go-live"></a>Napodobení ostrého provozu

Před uvedením do ostrého provozu musíte provést napodobení ostrého provozu pro otestování kroků potřebných pro přechod ze starších systémů na nový systém. Napodobení ostrého provozu byste měli provést v prostředí sandbox a zahrnout všechny kroky do svého plánu přechodu.

- Než přejdete do ostrého provozu, doporučujeme, abyste jako konfigurační prostředí GOLD používali provozní prostředí.
- Ujistěte se, že máte zaveden proces silné správy, který před uvedením do ostrého provozu chrání provozní prostředí před náhodnými transakcemi nebo aktualizacemi.
- Když jste připraveni provést UAT nebo napodobit ostrý provoz, aktualizujte prostředí sandbox z provozního prostředí. Další informace viz [Kopírování instance](hr-admin-setup-copy-instance.md).
- Vyzkoušejte každý krok svého plánu přechodu v prostředí sandbox a poté ověřte prostředí sandbox provedením namátkových kontrol nebo provedením testů ze skriptů UAT v daném prostředí.
  - Testy by měly zahrnovat všechny migrace dat včetně transformací potřebných pro uvedení do ostrého provozu.
  - Tento proces by měl zahrnovat faktické odstřižení od všech starších systémů.
  - Nezapomeňte do napodobení přechodu zahrnout všechny kroky integrace přechodu nebo kroky externího systému.
- Pokud se během napodobení přechodu vyskytnou nějaké problémy, může být vyžadováno druhé napodobení přechodu. Z tohoto důvodu doporučujeme zahrnout dva falešné přechody do plánu projektu.

## <a name="fasttrack-go-live-assessment"></a>Test naživo FastTrack

Zákazníci, kteří mají kvalifikaci pro FastTrack a jsou zapojeni do FastTrack Solution Architect, dokončí hodnocení přechodu do ostrého provozu s Microsoft FastTrack. Další informace viz  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Asi osm týdnů před uvedením do provozu vás tým FastTrack požádá o vyplnění [Kontrolního seznamu pro přechod od ostrého provozu](https://go.microsoft.com/fwlink/?linkid=2146013).

Manažer projektu nebo klíčový člen projektu musí během kontrolní fáze před zahájením projektu vyplnit kontrolní seznam uvedení do provozu. Kontrolní seznam je obvykle dokončen čtyři až šest týdnů před navrhovaným datem uvedení do provozu, kdy je UAT dokončen nebo téměř dokončen. 

Po dokončení kontrolního seznamu jej odešlete e-mailem svému architektovi řešení FastTrack. Na e-mail vždy uveďte klíčovou zúčastněnou stranu od zákazníka a implementačního partnera. 

Po odeslání kontrolního seznamu váš architekt řešení FastTrack zkontroluje projekt a poskytne posouzení, které popisuje potenciální rizika, osvědčené postupy a doporučení pro úspěšné uvedení projektu do provozu. V některých případech může architekt řešení upozornit na rizikové faktory a požádat o plán zmírnění. 

## <a name="see-also"></a>Viz také

[Často kladené dotazy týkající se ostrého nasazení](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]