---
title: Přidáno nastavení dodavatele pro náklady za doručení
description: Toto téma popisuje nová pole, která se přidají na stávající stránku Dodavatelé, když povolíte modul nákladů za doručení. Tato pole slouží k nastavení prodejců, které budete používat společně s funkcemi nákladů za doručení.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 3a288517f77d1618f94f8539506d01a108e63fa5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829755"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Přidáno nastavení dodavatele pro náklady za doručení

[!include [banner](../../includes/banner.md)]

Když povolíte modul **Náklady za doručení**, bude na existující stránku **Dodavatelé** přidáno několik nových polí. Tato pole slouží k nastavení prodejců, které budete používat společně s funkcemi nákladů za doručení.

Chcete-li nastavit příslušná pole, přejděte na **Zadávání veřejných zakázek a získávání zdrojů \> Prodejci \> Všichni prodejci**. Otevřete existujícího dodavatele nebo vytvořte nového dodavatele a poté vyberte záložku s náhledem **Různé podrobnosti**. Všechna nová pole, která přidává modul **Náklady za doručení**, se objeví pod nadpisem **Cesty**. Následující tabulka tato pole popisuje.

| Pole | popis |
|---|---|
| Typ přepravy | <p>Vyberte roli dodavatele ve vztahu k nákladům za doručení:</p><ul><li>**Žádný** - Dodavatel nemá žádnou konkrétní roli, která by souvisela s náklady za doručení. Tato hodnota je výchozí nastavení, protože většina dodavatelů pravděpodobně nebude mít žádnou konkrétní roli.</li><li>**Dopravní společnost** - Prodávající je dopravní společnost. Prodejci, kteří mají tento typ doručení, mohou být vybráni v poli **Dopravní společnost** na stránce **Plavby**.</li><li>**Celní makléř** - Dodavatel je celní makléř. Dodavatelé, kteří mají tento typ doručení, mohou být vybráni v poli **Celní makléř** na stránce **Folia**.</li><li>**Činidlo** - Dodavatel je agent. Dodavatelé, kteří mají tento typ doručení, mohou být vybráni v poli **Agent** na stránce **Dodavatelé** a **Nákupní objednávky**.</li></ul> |
| Skupina typu nákladů | Přiřazení dodavatele ke skupině typů nákladů za účelem výběru [automatických nákladů](auto-cost-setup.md). |
| Výchozí přístav | Vyberte přístav původu cesty. |
| Agent | Výchozí agent, když jsou nákupy prováděny od dodavatele. |
| Importovat dodavatele výpočtu nákladů | <p>Uveďte, zda je dodavatel dodavatelem pozemkových nákladů.</p><p>**Tip:** Toto pole můžete použít společně se zabezpečením na úrovni záznamu k omezení nákupních objednávek, které se zobrazují při vytváření cesty.</p> |
| Dopravní společnost | Vyberte výchozí přepravní společnost, která se použije při vytváření nákupních objednávek pro dodavatele. |
| Poskytovatel služeb | Uveďte, zda je dodavatel poskytovatelem služeb. |
| Nad/Pod skupinou tolerance | Vyberte výchozí skupinu tolerance nad / pod tolerancí pro dodavatele. |
