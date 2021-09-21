---
title: Množství není při registraci příchozích objednávek platné
description: 'Pokud množství, které je přiděleno pro registrační značku, překročí množství, které ještě musí být přijato pro aktuální dimenze, zobrazí se chybová zpráva: Množství není platné.'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475836"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Počet registračních značek není při registraci příchozích objednávek platný

## <a name="symptoms"></a>Příznaky

Když se pokusíte registrovat příchozí objednávky, může se zobrazit následující chybová zpráva:

> Množství není platné.

Pokud je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem* pro položku nabídky mobilního zařízení, která je použita k registraci příchozích objednávek, zobrazí se tato chybová zpráva a registraci nelze dokončit.

## <a name="cause"></a>Příčina

Když je *Definováno uživatelem* použito jako zásada pro seskupování registračních značek, systém rozdělí příchozí zásoby na samostatné registrační značky, jak udává skupina klasifikace jednotek. Pokud se ke sledování přijímané položky použije číslo dávky nebo sériové číslo, je třeba zadat množství každé dávky nebo série pro každou registrační značku, která je registrována. Pokud množství, které je zadáno pro registrační značku, překročí množství, které ještě musí být přijato pro aktuální dimenze, zobrazí se chybová zpráva.

## <a name="resolution"></a>Řešení

Když zaregistrujete položku pomocí položky nabídky mobilního zařízení, kde je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem*, může systém vyžadovat potvrzení nebo zadání čísel registračních značek, čísel dávek nebo sériových čísel.

Na potvrzovací stránce registrační značky systém zobrazí množství, které je přiděleno pro aktuální registrační značku. Na potvrzovací stránce dávky nebo série systém zobrazí množství, které ještě musí být přijato pro aktuální registrační značku. Bude také obsahovat pole, kde můžete zadat množství, které bude registrováno pro tuto kombinaci registrační značky a čísla dávky nebo sériového čísla. V takovém případě se ujistěte, že množství, které je registrováno pro registrační značku, nepřekročí množství, které ještě musí být přijato.

Případně pokud se při registraci příchozí objednávky vygeneruje příliš mnoho registračních značek, hodnotu pole **Zásady seskupování registračních značek** lze změnit na *Seskupení registračních značek*, položce lze přiřadit novou skupinu klasifikace jednotek nebo možnost **Seskupení registračních značek** pro skupinu klasifikace jednotek může být deaktivována.
