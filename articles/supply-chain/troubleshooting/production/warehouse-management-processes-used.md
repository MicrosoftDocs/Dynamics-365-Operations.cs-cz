---
title: Procesy řízení skladu se momentálně používají
description: Při rezervaci nebo uvolnění práce vám může přijít zpráva, že se aktuálně používají procesy správy skladu. Opravte problém pomocí jednoho z těchto kroků.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475748"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Nelze rezervovat nebo uvolnit práci, protože se aktuálně používají procesy

## <a name="symptoms"></a>Příznaky

Při práci s oddělenou výrobou se zobrazí následující chyba:

> Procesy řízení skladu se momentálně používají. Pokud řádky práce ještě nejsou zaregistrovány, můžete zrušit vytvořenou práci a jakékoli řádky vytížení nebo dodávky a poté pokračovat v procesu výdeje nebo dodávky.

## <a name="cause"></a>Příčina

K tomuto problému dochází, pokud se pokusíte rezervovat nebo uvolnit práci pro řádek, ale transakce zásob má stav *Vydáno*, což znamená, že materiál byl vydán.

## <a name="resolution"></a>Řešení

Chcete-li opravit problém, postupujte podle jednoho z následujících kroků.

- Změňte stav výrobní zakázky zpět na *Odhadováno* nebo *Uvolněno*.
- Otevřete stránku s podrobnostmi pro příslušnou výrobní zakázku. V podokně akcí na kartě **Sklad** ve skupině **Zastavit** vyberte **Zastavit a zrušit výdej** pro zrušení výdeje všech vydaných transakcí. Poté vyberte **Odebrat zastavení** a zpracujte výrobní zakázku.

Zde je vysvětlení funkcí *Zrušit výdej* a *Zastavit*:
  
- **Zrušit výdej** - Tato funkce stornuje stav transakcí zásob u řádků kusovníku a řádků vzorců, které mají stav od *Vydáno* po *Na objednávce*. Po dokončení práce pro výdej surovin je stav řádků nastaven na *Vydáno*. Tento stav zabrání resetování výrobní zakázky do stavu *Vytvořeno*. V tomto případě můžete použít funkci *Zrušit výdej* pro stornování transakcí ze stavu *Vydáno* a poté resetujte výrobní zakázku do stavu *Vytvořeno*.
- **Zastavit** - Tato funkce nastavuje příznak **Zastaveno** na výrobní zakázce, aby se zabránilo jakékoli aktualizaci stavu objednávky. Příznak **Zastaveno** naleznete na záložce s náhledem **Sklad** stránky s podrobnostmi o výrobní zakázce.

> [!NOTE]
>
> - Tlačítka jsou viditelná, pouze když je vytvořena výrobní zakázka pro položky, které jsou povoleny pro procesy skladu.
> - Skupina **Zastavit** je viditelná pouze na kartě **Sklad** v podokně akcí na stránce podrobností výrobní zakázky. Není viditelná na záložce s náhledem **Sklad** stránky se seznamem **Výrobní zakázky**.
