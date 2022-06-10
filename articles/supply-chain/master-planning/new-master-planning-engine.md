---
title: Migrace na optimalizaci plánování pro hlavní plánování
description: Toto téma poskytuje informace o novém modulu hlavního plánovací, optimalizaci plánování, a o migraci ze stávajícího modulu.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 598e29ead50e1ecb249a7338c7f0952a912b4f69
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809088"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migrace na optimalizaci plánování pro hlavní plánování

[!include [banner](../includes/banner.md)]

Integrovaný modul hlavního plánování je naplánován tak, aby byl brzy vyřazen (zastaralý). Nahrazuje ho doplněk Optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management. Toto téma poskytuje informace o dopadu na nová a stávající nasazení. Obsahuje informace o požadovaných akcích.

Optimalizace plánování umožňuje, aby výpočty hlavního plánování byly prováděny mimo Supply Chain Management a jeho databázi Azure SQL. Výhody, které jsou přidruženy k optimalizaci plánování, zahrnují lepší výkon a minimalizovaný dopad na databázi SQL během spuštění hlavního plánování. Protože rychlé plánování lze provést i v průběhu pracovní doby, plánovači mohou ihned reagovat na požadavky nebo změny parametrů.

Další informace o optimalizaci plánování naleznete v tématu [Přehled optimalizace plánování](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Zastaralost stávajícího modulu hlavního plánování

Microsoft se chystá vestavěný plánovací modul vyřadit ve prospěch optimalizace plánování. Tato změna ovlivní všechna cloudová prostředí. Místní instalace nejsou ovlivněny. Ve verzi 10.0.16 a novější se zobrazí chybová zpráva, pokud spustíte integrované hlavní plánování bez generování plánovaných výrobních zakázek. Spuštění hlavního plánování však bude úspěšně dokončeno i přes chybovou zprávu.

Další informace o zastaralosti integrovaného plánovacího modulu najdete v oznámeních v části [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migrace, zprávy a výjimky

Vlastníci stávajících prostředí, kteří provozují vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky. Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.

Jak bylo zmíněno, ve verzi 10.0.16 a novější se zobrazí chybová zpráva, pokud spustíte integrované hlavní plánování bez generování plánovaných výrobních zakázek. Tato chybová zpráva obsahuje pokyny k migraci a pokyny pro vyžádání výjimky.

### <a name="new-deployments"></a>Nová nasazení

Optimalizace plánování musí být považována za výchozí hlavní plánovací modul pro všechna nová nasazení v cloudu. Optimalizace plánování by se měla obecně použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky. Pokud nové nasazení závisí na funkčnosti, kterou Optimalizace plánování aktuálně nepodporuje, můžete požádat o výjimku, abyste mohli i nadále používat integrovaný hlavní plánovací modul.

### <a name="existing-deployments"></a>Stávající nasazení

Vlastníci stávajících cloudových nasazení, která závisí na hlavním plánování, by měli plánovat migraci na Optimalizaci plánování. Pokud vaše implementace závisí na funkčnosti, kterou Optimalizace plánování aktuálně nepodporuje, můžete požádat o výjimku, abyste mohli i nadále používat integrovaný hlavní plánovací modul.

V prostředích, která aktuálně používají hlavní plánovací procesy, které jsou zastaralé, zašle Microsoft e-mail správci prostředí. Tento e-mail poskytne informace o akcích, které jsou nutné k migraci nebo k žádosti o výjimku.

## <a name="the-exception-process"></a>Proces výjimky

Pokud musíte i nadále používat integrovaný hlavní plánovací modul, můžete požádat o výjimku, protože vaše obchodní procesy silně závisí na alespoň jedné funkci, která není aktuálně implementována v optimalizaci plánování. Seznam dostupných funkcí naleznete v části [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization/planning-optimization-fit-analysis.md).

V současné době jsou výjimky pro migraci optimalizace plánování relevantní pouze v případě, že váš hlavní plánovací proces nezahrnuje výrobu (tj. plánované výrobní zakázky generované hlavním plánováním) a vyžadujete vestavěný modul hlavního plánování po verzi 10.0.15.

Poté, co budou k dispozici požadované funkce, poskytne Microsoft období odkladu do vypršení platnosti výjimky. Správce prostředí bude informován, až budou k dispozici požadované funkce a začne období odkladu.

Následující vývojový diagram shrnuje informace uvedené v tomto tématu, takže můžete rychle zjistit, zda byste měli požádat o výjimku. Pokud potřebujete požádat o výjimku, vyplňte a odešlete [Dotazník pro plánování optimalizace migrace a výjimky](https://go.microsoft.com/fwlink/?linkid=2144962). Za vyhodnocení a schvalování každé žádosti o výjimku je zodpovědná produktová skupina, proto pomocí uvedeného odkazu odešlete žádost přímo produktové skupině a nevytvářejte pro ni lístek podpory. Pokud bude váš požadavek zamítnut, nevytvářejte lístek podpory, protože podpora společnosti Microsoft nemůže přehodnotit ani udělit výjimky.

![Vývojový diagram výjimek.](media/exception-diagram.png "Vývojový diagram výjimek")

> [!NOTE]
> Výjimku můžete požadovat pouze pro klienty, kteří aktuálně zahrnují nebo budou zahrnovat provozní prostředí, nikoli pouze pro klienty s izolovanými prostředími. Pokud potřebujete zakázat chybu výjimky optimalizace plánování v sandboxovém prostředí infrastruktury jako služby (IaaS), spusťte dotaz SQL uvedený v části [Sandboxová prostředí](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandboxová prostředí

Mohu ve svém sandboxovém prostředí použít integrované hlavní plánování? Potřebuji výjimku?

**Odpověď:** Výjimky nejsou obvykle relevantní pro sandboxová prostředí, protože chyba výjimky optimalizace plánování nezabrání úspěšnému spuštění integrovaného hlavního plánovacího modulu. Pokud vás však chybová zpráva vyrušuje, můžete ji v sandboxovém prostředí IaaS (nikoliv Service Fabric) zakázat spuštěním následujícího dotazu ve vaší databázi:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Místní prostředí

Moje prostředí je místní. Potřebuji výjimku?

**Odpověď:** Ne. Pro místní prostředí se nevyžaduje výjimka. Můžete pokračovat v používání integrovaného hlavního plánování. Pokud bude vyžadována nějaká akce, bude váš správce prostředí informován.

### <a name="production-scenarios"></a>Produkční scénáře

Používáme plánované výrobní zakázky, ale obávám se, co se stane, když upgradujeme na verzi 10.0.16. Mám podniknout nějaké kroky?

**Odpověď:** Nemělo by vás to znepokojovat. Můžete pokračovat v používání integrovaného hlavního plánování ve verzi 10.0.16. Doporučujeme však vyhodnotit, zda migrace na optimalizaci plánování může začít s aktuální funkcí. Doporučujeme také, abyste se informovali o nových funkcích.

### <a name="email-from-microsoft"></a>E-mail od společnosti Microsoft

Náš správce prostředí obdržel e-mail od společnosti Microsoft. Tento e-mail uvádí, že bychom měli přejít na optimalizaci plánování nebo požádat o výjimku. Musím něco podniknout?

**Odpověď:** Ano. Vaše prostředí bude ovlivněno, pokud nebudete postupovat podle pokynů v e-mailu. Můžete buď migrovat na Optimalizaci plánování do uvedeného data, nebo požádat o výjimku pomocí odkazu v e-mailu. Tento odkaz otevře dotazník. Po vyplnění a odeslání tohoto dotazníku obdržíte e-mailem odpověď. Ačkoli je tento proces manuální, Microsoft se pokusí odpovědět do týdne po odeslání dotazníku.

### <a name="error-messages"></a>Chybové zprávy

Používám verzi 10.0.16 nebo novější a při spuštění hlavního plánování se mi zobrazí následující chybová zpráva. Je hlavní plánování blokováno?

> Tato chybová zpráva se zobrazí, protože předdefinovaný hlavní plánovací modul byl použit pro scénáře podporované optimalizací plánování. Měli byste migrovat na optimalizaci plánování hned teď, protože aktuální vestavěné hlavní plánování bude zastaralé. Všimněte si, že toto spuštění hlavního plánování bylo úspěšně dokončeno.
>
> V případě, že vaše migrace má silné závislosti na čekajících funkcích, lze požádat o výjimku z dalšího používání integrovaného hlavního plánovacího modulu.
>
> Chcete-li začít, vyplňte prosím následující dotazník a případně požádejte o výjimku z migrace na optimalizaci plánování.

**Odpověď:** Ne, hlavní plánování není blokováno. Vaše spuštění hlavního plánování bylo úspěšně dokončeno a výsledek můžete použít obvyklým způsobem. Chcete-li se však vyhnout dostávání této chybové zprávy během budoucích spuštění hlavního plánování, musíte buď migrovat na optimalizaci plánování okamžitě, nebo požádat o výjimku pomocí odkazu v chybové zprávě.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
