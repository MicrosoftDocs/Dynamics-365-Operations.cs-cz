---
title: Optimalizace naplánovaných dávkových úloh BYOD
description: Toto téma vysvětluje, jak optimalizovat výkon, když používáte funkci použití vlastní databáze (BYOD) s řešením Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4b9cf4b4181b64ef4daf397edd852fb2f881424e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111706"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Optimalizace naplánovaných dávkových úloh BYOD

Toto téma vysvětluje, jak optimalizovat výkon, když používáte funkci použití vlastní databáze (BYOD). Další informace o BYOD viz [Použití vlastní databáze (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).

## <a name="performance-considerations-for-data-export"></a>Zvážení výkonu pro export dat

Po publikování entit v cílové databázi můžete použít funkci Exportovat v pracovním prostoru **Správa dat** pro přesun dat. Funkce exportu vám umožňuje definovat úlohu přesnunu dat, která obsahuje jednu nebo více entit. Další informace, jak používat exportovat data, naleznete v tématu [Přehled úloh importu a exportu dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).

Stránku **Export** můžete použít pro export dat do různých cílových datových formátů, například souboru CSV. Tato stránka podporuje také databáze SQL jako další cíl.

Můžete vytvořit datový projekt, který má více entit, a pomocí dávkové úlohy naplánovat spuštění tohoto datového projektu. Pokud vyberete možnost **Exportovat v dávce**, můžete naplánovat pravidelné spouštění úlohy exportu dat.

Chcete-li zachovat celkovou spolehlivost exportu BYOD, musíte být opatrní, když do projektu exportu přidáte více entit. Když určujete počet entit, které se mají přidat do stejného projektu, zvažte následující parametry:

- Složitost entit
- Očekávaný objem dat na entitu
- Celková doba potřebná k dokončení exportu na úrovni úlohy

Pro nejlepší výkon nepřidávejte stovky entit do jednoho projektu. Doporučujeme vytvořit více úloh, z nichž každá obsahuje méně entit.

## <a name="scheduling-byod-batch-jobs"></a>Plánování dávkových úloh BYOD

Pro snížení dopadu na uživatele řešení Microsoft Dynamics 365 Human Resources spusťte dávkové úlohy BYOD v noci nebo po pracovní době. U opakujících se dávkových úloh zkontrolujte časové pásmo. Některé dávkové úlohy mohou používat tichomořský standardní čas (PST).

Abyste se vyhnuli problémům s výkonem, zvažte při konfiguraci frekvence plánování pro dávkové úlohy BYOD následující faktory:

- Čas potřebný k dokončení každé dávkové úlohy
- Obchodní potřeby pro data v BYOD

Nastavte frekvenci pro každou dávkovou úlohu na hodnotu, která zajistí, že bude možné úlohu dokončit dlouho před jejím dalším plánovaným časem spuštění. Vyhněte se paralelnímu spuštění více úloh, protože tento přístup může negativně ovlivnit výkon aplikace Human Resources.

Pro nejlepší výkon vždy používejte možnost **Exportovat v dávce** na stránce **Export** pro plánování dávkových úloh BYOD. Vyhněte se plánování opakujících se exportů v **Spravovat \> Spravovat opakující se datové úlohy**.

## <a name="incremental-export"></a>Přírůstkový export

Když přidáte entitu pro export dat, můžete provést buď přírůstkové nabízení (export) nebo úplné nabízení. Úplné nabízení odstraní všechny existující záznamy z entity v databázi BYOD. Poté vloží aktuální sadu záznamů z entity Human Resources.

Chcete-li provést přírůstkové nabízení, musíte zapnout sledování změn pro každou entitu na stránce **Entity**. Další informace viz [Povolení sledování změn pro entity](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

Pokud vyberete přírůstkové nabízení, první nabázení je vždy úplné nabízení. SQL sleduje změny od tohoto prvního úplného nabízení. Když je vložen nový záznam nebo když je záznam aktualizován nebo odstraněn, změna se projeví v cílové entitě.

## <a name="time-outs"></a>Časové limity

Zde jsou výchozí časové limity pro exporty BYOD:

- Deset minut na operace zkrácení
- Jedna hodina pro operace hromadného vkládání

Pokud jsou objemy dat vysoké, nemusí tato nastavení časového limitu stačit. Chcete-li je aktualizovat, přejděte na **Správa dat \> Parametry architektury \> Použití vlastní databáze**. Tyto časové limity jsou specifické pro společnost a musí být nastaveny zvlášť pro každou společnost.

## <a name="known-limitations"></a>Známá omezení

Funkce BYOD má následující omezení:

- Během synchronizace by ve vaší databázi neměly být žádné aktivní zámky. Aktivní zámky mohou způsobit pomalé zápisy nebo dokonce selhání exportu dat do vaší databáze Azure SQL.
- Složené entity nelze exportovat do vlastní databáze. V současné době nejsou složené entity podporovány. Musíte exportovat jednotlivé entity, které tvoří složenou entitu. Můžete však exportovat obě entity ve stejném datovém projektu.
- Entity, které nemají jedinečné klíče, nelze exportovat pomocí přírůstkového nabízení. S tímto omezením se můžete setkat, zvláště když se pokoušíte přírůstkově exportovat záznamy z několika připravených entit. Protože tyto entity byly navrženy tak, aby umožňovaly import dat, nemají jedinečný klíč.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="incremental-push-doesnt-work-correctly"></a>Přírůstkové nabízení nefunguje správně

**Problém:** Když dojde k úplnému nabízení pro entitu, uvidíte velkou sadu záznamů v BYOD, když použijete příkaz **select**. Když však provedete přírůstkové nabízení, uvidíte v BYOD jen několik záznamů. Zdá se, jako by přírůstkové nabízení odstranilo všechny záznamy a přidalo pouze změněné záznamy v BYOD.

**Řešení:** Tabulky sledování změn SQL nemusí být v očekávaném stavu. V případech tohoto typu doporučujeme vypnout sledování změn pro entitu a poté ji znovu zapnout. Další informace viz [Povolení sledování změn pro entity](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

## <a name="see-also"></a>Viz také

[Přehled správy dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[Použití vlastní databáze (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[Přehled úloh importu a exportu dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[Povolení sledování změn pro entity](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]