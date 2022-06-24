---
title: Přehled správy technických změn (obsahuje video)
description: Tento článek poskytuje přehled správy technických změn, která vám pomůže plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6c9bfcdef91ad07b8346498b8944e1d741d623a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862649"
---
# <a name="engineering-change-management-overview"></a>Přehled správy technických změn

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Souhrn funkce

Dnešní výrobci vyžadují silnou správu dat produktu, řízení verzí a správu technických změn, aby uspěli ve světě neustále se snižujících životních cyklů produktů, zvýšených požadavků na kvalitu a spolehlivost a zvýšeného zaměření na bezpečnost produktů.

Správa technických změn přináší strukturu a disciplínu do procesu správy dat produktu a umožňuje, aby byly produkty definovány, uvolňovány a revidovány kontrolovaným způsobem, který je podporován pracovními postupy. Prostřednictvím verzí produktu a správy technických změn můžete dokumentovat, hodnotit dopad a aplikovat technické změny během celého životního cyklu produktu.

Správa technických změn vám pomáhá plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn. Zde je seznam jejich hlavních funkcí:

- Verzování produktu
- Vylepšená funkce uvolňování produktu, která vám umožní udržovat hlavní data produktu v jedné právnické osobě (technická společnost) a publikovat plně nakonfigurovaný uvolněný produkt do jiných právnických společností.
- Pravidla pro ověřování, zda jsou požadované informace zadány před aktivací verze produktu (kontroly připravenosti).
- Vylepšená správa životního cyklu produktu prostřednictvím detailní kontroly nad tím, kdy lze uvolněný produkt použít v konkrétních obchodních procesech.
- Požadavky na technické změny, které jsou podporovány pracovními postupy
- Příkazy k technickým změnám, které jsou podporovány pracovními postupy

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Předchozí video ([Možnosti správy změn v Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) je součástí seznamu videí o [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), které jsou k dispozici na YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Zapněte pro svůj systém funkce správy technických změn

Než budete moci používat funkci správy technických změn, musíte povolit funkci *správy technických změn* a její konfigurační klíč. Pokud chcete také sledovat dimenzi verze produktů v transakcích (volitelně), musíte povolit také funkci *Dimenze verze produktu* a její konfigurační klíč. Po nastavení těchto předpokladů podle potřeby budete moci zapnout další volitelné funkce pro správu technických změn.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Zapnutí nebo vypnutí základní funkce správy technických změn

Chcete-li zapnout nebo vypnout základní funkci správy technických změn, postupujte takto. Od verze Supply Chain Management 10.0.25 je funkce *Správa technických změn* ve výchozím nastavení zapnuta.

1. Přejděte do [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Zkontrolovat aktualizace.
1. Podle potřeby zapněte nebo vypněte funkci s názvem *Správa technických změn*.
1. Pokud chcete sledovat dimenzi verze produktů v transakcích (volitelně), zapněte funkci *Verze dimenze produktu*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Zapnutí nebo vypnutí požadovaných konfiguračních klíčů

Správci mohou zapnout konfigurační klíče provedením následujících kroků. Implicitně nejsou zapnuté.

1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Rozbalte uzel **Obchod**.
1. Povolte nebo zakažte konfigurační klíč pro hlavní funkci výběrem zaškrtávacího políčka **Správa technických změn**.
1. Rozbalte uzel **Řízení technických změn** a podle potřeby zaškrtněte nebo zrušte zaškrtnutí následujících políček (v závislosti na funkcích, které chcete použít):

    - **Hledání atributů** - Zaškrtnutím tohoto políčka povolíte [funkce vyhledávání atributů](engineering-attributes-and-search.md). Doporučujeme tuto funkci povolit, ale pokud ji nepoužíváte, můžete toto zaškrtávací políčko zrušit.
    - **Řízení změn pro procesní výrobu** - Toto políčko zaškrtněte, pokud chcete pomocí funkcí správy technických změn spravovat změny ve vzorcích pro procesní výrobu. Pokud vzorce nemusíte spravovat, můžete toto zaškrtávací políčko zrušit. Další informace viz [Spravujte změny v recepturách a jejich látkách](manage-formula-changes.md).

1. Chcete-li také použít dimenzi verze, zaškrtněte také políčko **Dimenze produktu - verze**. (Toto zaškrtávací políčko je pod seznamem, není vnořeno do uzlu **Správa technických změn**.) Vypněte toto políčko, pokud tuto funkci nepotřebujete.
1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Databáze musí být synchronizována, aby bylo zajištěno, že jsou konfigurační klíče správně aktualizovány, aby reagovaly na provedené změny. Proveďte jeden z následujících kroků v závislosti na typu prostředí, na kterém pracujete:
    - **Pro prostředí úrovně 1 (vývoj)**: Otevřete svůj projekt v Microsoft Visual Studio a poté vyberte **Dynamics 365 \> Synchronizovat databázi \> Synchronizovat**.
    - **Pro prostředí úrovně 2 (a vyšší)**: Databáze se automaticky synchronizuje poté, co prostředí přepnete do režimu údržby a odejdete z něj, takže tento krok můžete přeskočit.

### <a name="turn-on-additional-engineering-change-management-features"></a>Zapněte pro svůj systém další funkce správy technických změn

Poté, co zapnete základní funkce správy technických změn a povolíte jejich konfigurační klíče, bude do správy funkcí přidáno několik dalších a volitelných funkcí správy technických změn. Každá z těchto funkcí je uvedena v modulu **Řízení technických změn**. Následující tabulka popisuje každou volitelnou funkci a poskytuje odkazy na další informace. Od verze Supply Chain Management verze 10.0.25 jsou všechny tyto funkce ve výchozím nastavení zapnuty, ale stále je můžete vypnout.

| Název funkce ve správě funkcí | Popis | Stav funkce |
|---|---|---|
| Povolení správy změn u stávajících produktů | <p>Tato funkce vám umožňuje převést stávající produkty na technické produkty, abyste je mohli začít spravovat pomocí správy technických změn.</p><p>Další informace naleznete v tématu [Povolení změnového řízení u existujících produktů](change-management-existing-products.md).</p> |
| Technická oznámení pro výrobu | <p>Když se produkt změní v technickém zpracování, může být důležité informovat výrobu o těchto změnách. Pracovníci ve výrobě tak mohou podniknout příslušná opatření, jako je náhrada součástí, výměna kusovníku nebo výměna trasy. Tato funkce vám umožňuje informovat produkci o změnách vyráběných produktů.</p><p>Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).</p> |
| Vylepšená dědičnost atributů pro Řízení technických změn | <p>Tato funkce zjednodušuje správu atributů pro hotové výrobky nebo meziprodukty. Když je tato funkce zapnutá, je snazší identifikovat všechny atributy, které patří k položce, a můžete vybrat atributy, které se mají šířit z této položky do její nadřazené položky. Tato funkce je užitečná, když je například jedna složka hotového zboží křehká, toxická nebo hořlavá, protože křehký, toxický nebo hořlavý atribut můžete snadno identifikovat a šířit do hotového zboží.</p><p>Další informace viz [Technické atributy a vyhledávání technických atributů](engineering-attributes-and-search.md).</p> |
| Kontroly připravenosti produktu | <p>Tato funkce umožňuje nastavit kontroly připravenosti na standardní (netechnické) produkty. Pomocí kontroly připravenosti produktu zajistěte, aby byl každý produkt plně definován a aby byly nakonfigurovány všechny požadované zásady, než bude produkt zpřístupněn a použit v transakcích. Pokud tuto funkci po chvíli použijete, všechny stávající kontroly připravenosti standardních produktů budou odstraněny.</p><p>Další informace naleznete v tématu [Připravenost produktu](product-readiness.md).</p> |
| Spravujte změny v recepturách a jejich látkách | <p>Tato funkce vám umožní sledovat změny přísad, vedlejších produktů a doprovodných produktů.</p><p>Další informace viz [Spravujte změny v recepturách a jejich látkách](manage-formula-changes.md).</p> |
| Generování varianty pro technické produkty | <p>Tato funkce vám umožňuje generovat varianty pro technické produkty na základě dostupných hodnot dimenzí.</p><p>Další informace viz [Generování variant pro strojírenské výrobky](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
