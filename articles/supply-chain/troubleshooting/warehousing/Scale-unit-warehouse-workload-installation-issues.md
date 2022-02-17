---
title: Problémy při zpracování, ke kterým dojde po instalaci úlohy jednotky škálování pracovního vytížení skladu
description: Toto téma popisuje problémy, které se mohou vyskytnout brzy po instalaci úlohy jednotky škálování pracovního vytížení skladu, a poskytuje rady pro jejich odstranění.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071622"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Problémy při zpracování, ke kterým dojde po instalaci úlohy jednotky škálování pracovního vytížení skladu

Toto téma popisuje problémy, které se mohou vyskytnout brzy po instalaci úlohy jednotky škálování pracovního vytížení skladu, a poskytuje rady pro jejich odstranění.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Problém 1: Chyba po uvolnění vytížení z pracovní plochy plánování vytížení

### <a name="symptoms-of-issue-1"></a>Příznaky problému 1

Když uvolníte vytížení ze stránky **Pracovní plocha plánování vytížení** nebo **Pracovní plocha pro plánování odchozího vytížení**, zobrazí se chybová zpráva, která má následující tvar:

> Při zaúčtování vytížení byla zachycena výjimka %1, vytížení nelze uvolnit.
> 
> UPDATE WHSSHIPMENTTABLE SET ...
> 
> Nelze upravit záznam v Dodávkách (WHSShipmentTable). ID dodávky: ...

Zde je skutečný příklad, který obsahuje ukázková data:

> Při zaúčtování vytížení USMF-00003 byla zachycena výjimka, vytížení nelze uvolnit.
relace 5133 (administrátor)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? WHERE ((RECID=?) AND (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 pro SQL Server][SQL Server]Scale Unit @@ se pokusil aktualizovat záznamy vlastněné jednotkou škálování @A.  
> Object Server Azure:
>
> Nelze upravit záznam v Dodávkách (WHSShipmentTable). ID dodávky: USMF-000031, USMF-000033. Databáze SQL vrátila chybu.

### <a name="cause-of-issue-1"></a>Příčina problému 1

K tomuto problému může dojít, pokud při instalaci jednotky škálování pracovního vytížení skladu existuje následující kombinace podmínek:

- Systém zahrnuje neuvolněné vytížení, kde je několik řádků spojeno s různými objednávkami a některé řádky vytížení nejsou spojeny s dodávkou.
- Systém je nastaven tak, aby používal konsolidaci dodávek.

V distribuovaném nasazení s hybridní topologií je každý záznam o vytížení a dodávce označen jako vlastněný konkrétní jednotkou škálování nebo centrem. Když uvolníte vytížení na stránce **Pracovní plocha plánování vytížení**, systém změní přiřazené vlastnictví. Kvůli výše uvedeným podmínkám však systém nemusí být schopen vyřešit vlastnictví dat. Proto se mu nepodaří uvolnit vytížení do skladu.

### <a name="resolution-of-issue-1"></a>Řešení problému 1

Než vytížení uvolníte do skladu, rozdělte jej na dvě menší vytížení.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Problém 2: Chyba při zpracování vlny v jednotce škálování

### <a name="symptoms-of-issue-2"></a>Příznaky problému 2

Když zpracováváte vlnu na jednotce škálování, zobrazí se chybová zpráva, která má následující tvar:

> Nemůžete upravit řádek vytížení s RecId = %1, id vytížení = %2, protože je stále ve vlastnictví podnikového centra. Ujistěte se prosím, že odpovídající odchozí vytížení bylo uvolněno do jednotky škálování a tím byly vytvořeny řádky skladové objednávky.

Zde je skutečný příklad, který obsahuje ukázková data:

> Informační protokol pro úlohu Execute Wave USMF-000000012 (9223377668365210)  
> Informační protokol pro úlohu Execute Wave USMF-000000012 (9223377668370462)  
> Nemůžete upravit řádek vytížení s RecId = 68719478242, id vytížení = USMF-000034, protože je stále ve vlastnictví podnikového centra. Ujistěte se prosím, že odpovídající odchozí vytížení bylo uvolněno do jednotky škálování a tím byly vytvořeny řádky skladové objednávky.

### <a name="cause-of-issue-2"></a>Příčina problému 2

V distribuovaném nasazení s hybridní topologií je vlastnictví vytížení a data dodávky přiřazeno ke konkrétní jednotkce škálování nebo centru. V rámci zpracování vlny se očekává, že vlastnictví dat bude přiřazeno jednotce škálování.

Když nainstalujete jednotku škálování pracovního vytížení skladu a otevřená zásilka je spojena s vytížením a vlnou, systém nemůže řídit vlastnictví dat. Zpracování vlny proto v jednotce škálování selže.

### <a name="resolution-of-issue-2"></a>Řešení problému 2

Uvolněte vytížení z centra do skladu.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Řešení problémů zobrazením vlastnictví a cíle záznamu

V distribuovaném nasazení s hybridní topologií jsou mnohé typy záznamů označeny jako vlastněné konkrétní jednotkou škálování nebo centrem. Poté, co přepnete na distribuovanou hybridní topologii a/nebo nastavíte novou jednotku škálování pracovního vytížení skladu, systém přiřadí vlastnictví každému příslušnému záznamu. Tento proces může někdy způsobit chyby nebo vést k neočekávaným výsledkům. Informace o vlastnictví záznamu a cíli přenosu vám proto mohou pomoci při odstraňování problémů, které nastanou po provedení těchto typů změn.

Chcete-li zobrazit vlastnictví a cíl převodu záznamu, postupujte takto.

1. Otevřete relevantní záznam.
1. V podokně akcí na kartě **Možnosti** ve skupině **Informace o záznamu** vyberte **Zobrazit všechna pole**.
1. Stránka, která se zobrazí, zobrazuje hodnoty pro všechna pole, které jsou k dispozici ve vybraném záznamu. Zkontrolujte následující pole:

    - **SYSSCALEUNITID** – Toto pole zobrazuje aktuálního vlastníka záznamu.
    - **SYSTARGETSCALEUNITID** – Toto pole zobrazuje ID jednotky škálování centra nebo jednotku škálování, do které bude záznam přenesen, až s ním aktuální vlastník skončí. Hodnotu tohoto pole používají dávkové úlohy, které řídí tento typ procesu. Ačkoli toto pole přímo nesouvisí s vlastnictvím, může se vlastnictví změnit, když je záznam převeden. V některých případech bude toto pole prázdné.
