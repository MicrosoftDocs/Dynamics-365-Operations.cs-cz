---
title: Instalace, nastavení a aktualizace zákaznického portálu
description: V tomto tématu jsou uvedeny podrobné informace o licencích a pokyny k nastavení zákaznického portálu.
author: dasani-madipalli
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5c4cad305e3d130b3283ca3424c84f60e2d13307
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907808"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Instalace, nastavení a aktualizace zákaznického portálu

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Požadavky na licence

Chcete-li implementovat zákaznický portál, musíte mít následující licence:

- **Portály Power Apps** - Tato licence je nutná k hostování zákaznického portálu. Portály jsou licencovány na základě použití. Pro více informací viz [Licenční požadavky na portály Power Apps](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Dvojí zápis** - Musíte mít potřebné licence, abyste mohli aktivovat dvojí zápis pro tabulky Supply Chain Management. Další informace naleznete v tématu [Systémové požadavky pro dvojí zápis](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Závislosti na dvojím zápisu a portálech Power Apps

Zákaznický portál závisí na portálech Power Apps a duálním zápisu, jak ukazuje následující obrázek.

![Závislosti zákaznického portálu](media/customer-portal-elements.png "Závislosti zákaznického portálu")

Na rozdíl od jiných funkcí Supply Chain Management sídlí šablona zákaznického portálu v portálech Power Apps. Zákaznický portál je proto omezen funkcemi a možnostmi, které poskytují portály Power Apps a tabulky v dvojím zápisu.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Požadované nastavení pro aktivaci zákaznického portálu

Poté, co jste se ujistili, že máte požadované licence, můžete nastavit duální zápis, jak je popsáno v [pokynech pro počáteční synchronizaci s dvojím zápisem](/dynamics365/supply-chain/sales-marketing/enable-entity-map).

U duálního zápisu nezapomeňte povolit následující mapování tabulek:

- Záhlaví prodejní objednávky
- Detaily prod. objednávky
- Účty
- Kontakty
- Produkty

Po dokončení tohoto nastavení můžete poskytnout šablonu zákaznického portálu.

## <a name="provision-the-customer-portal"></a>Zřízení zákaznického portálu

Než začnete, ujistěte se, že jste již dokončili [požadované nastavení](#required-setup). Poté postupujte podle těchto pokynů a vytvořte zákaznický portál.

1. Přejděte na [make.powerapps.com](https://make.powerapps.com/).
2. Ujistěte se, že používáte prostředí, ve kterém jste povolili duální zápis.
3. Na kartě **Vytvořit** přejděte dolů do sekce **Začít od šablony** a vyberte šablonu s názvem **Zákaznický portál**.
4. Postupujte podle pokynů na obrazovce.

Po dokončení zřizování máte přístup na zákaznický portál v části **Vaše aplikace** na **Domovské** stránce.

> [!NOTE]
> Pokud řešení duálního zápisu není nainstalované v prostředí, ve kterém pracujete, zobrazí se chybová zpráva a zákaznický portál nebude zajištěn.

## <a name="update-the-customer-portal"></a>Aktualizace zákaznického portálu

Další funkce mohou být přidány do zákaznického portálu později. Jakékoli změny, které společnost Microsoft provede u základních komponent řešení, se automaticky objeví ve vašem prostředí. Web poskytnutý ve vašem prostředí však nebude automaticky odrážet změny provedené v konfiguračních datech. Tyto změny budete muset použít ručně tak, že získáte kód z nové šablony a sloučíte jej s poskytnutým webem.

## <a name="additional-resources"></a>Další prostředky

Chcete-li se dozvědět, jak můžete nastavit a přizpůsobit zákaznický portál, měli byste začít prostudováním následující dokumentace pro základní technologie:

- [Dokumentace portálů Power Apps](/powerapps/maker/portals/overview)
- [Dokumentace dvojitého zápisu](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Abyste mohli účinně spravovat své portály, musíte porozumět portálům Power Apps a životním cyklům Microsoft Dataverse. Další informace naleznete v následujících zdrojích:

- [O životním cyklu portálu](/powerapps/maker/portals/admin/portal-lifecycle)
- [Upgradujte portál](/powerapps/maker/portals/admin/upgrade-portal)
- [Migrace konfigurace portálu](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Správa životního cyklu řešení: aplikace Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]