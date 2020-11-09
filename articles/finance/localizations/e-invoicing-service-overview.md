---
title: Přehled doplňku Elektronická fakturace
description: Toto téma poskytuje informace o doplňku elektronické fakturace v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039739"
---
# <a name="electronic-invoicing-add-on-overview"></a>Přehled doplňku Elektronická fakturace

[!include [banner](../includes/banner.md)]

Doplněk elektronické fakturace pro Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management je hyperškálovatelná multiklientová služba, která umožňuje konfigurovatelné zpracování dokumentů elektronických faktur a konfigurovatelnou výměnu dokumentů. Pravidla zpracování a integrace jsou plně konfigurovatelná a logika je spuštěna mimo Finance a Supply Chain Management. Služba je zaměřena hlavně na zpracování eleltronických faktur ve scénářích podniky-vláda, ale lze ji přizpůsobit i pro jiné účely.

Doplněk elektronické fakturace vám pomůže dosáhnout následujících cílů:

- Rychlé a snadné přijetí požadavků konkrétních zemí / regionů
- Standardizované implementace doplňkového řešení elektronické fakturace
- Vylepšená sledovatelnost historie dokumentů
- Kratší implementační cyklus
- Snížené celkové náklady na vlastnictví (TCO)
- Snadno nastavitelné konfigurace, které nevyžadují změny kódu
- Zjednodušené konfigurační balení
- Integrovaný export, import a integrace a snadná rozšiřitelnost při zpracování dokumentů elektronických faktur
- Snadné opětovné použití stejné konfigurace exportu, importu a integrace napříč společnostmi

Chcete-li použít doplněk Elektronická fakturace, musíte jej nainstalovat ze svého projektu v Microsoft Dynamics Lifecycle Services (LCS). Dále podle postupu nastavení zapněte integraci s Finance nebo Supply Chain Management. Více informací viz [Začněte s doplňkem elektronické fakturace](e-invoicing-get-started.md).

## <a name="availability"></a>Dostupnost

Zpočátku je doplněk Elektronická fakturace k dispozici vybraným zákazníkům prostřednictvím programu náhledu. Později se náhled otevře širšímu okruhu zákazníků. Nakonec bude služba obecně dostupná. Protože funkce, která řeší požadavky specifické pro zemi / region, mohou být v různých fázích vydání omezené, měli byste vždy zkontrolovat nejaktuálnější dokumentaci, která zdůrazňuje pokrytí a rozsah podporovaných řešení pro konkrétní zemi / region.

Doplněk elektronické fakturace je nasazen v následujících geografických oblastech Azure:

- Spojené státy americké
- Evropa

> [!NOTE]
> Doplněk elektronické fakturace nepodporuje místní nasazení.

## <a name="extended-configurability"></a>Rozšířená konfigurovatelnost

Doplněk elektronické fakturace lze použít ve scénářích, kdy musíte vytvořit a odeslat elektronický dokument určeným stranám. Je speciálně navržen pro spuštění konfigurovatelného toku akcí zpracování na základě přijatých dat. Možnosti konfigurovatelnosti, které jsou k dispozici v oblasti Finance a Supply Chain Management, jsou omezeny na transformaci dokumentů. Služba rozšiřuje tyto možnosti přidáním konfigurovatelných integrací, které jsou v ní k dispozici. Kromě toho všechny funkce elektronických faktur, které byly dříve k dispozici, například brazilská Nota fiscal eletrônica (NF-e), mexická Comprobante Fiscal Digital por Internet (CFDI) nebo jiný západoevropský univerzální obchodní jazyk (UBL) / Pan-European Public Procurement OnLine (PEPPOL) budou používat konfigurace pro export a import a pro umožnění integrace s externími webovými službami.

## <a name="feature-highlights"></a>Zvýrazněné funkce

- Dodávaná integrace s Finance a Supply Chain management
- Konzistentní uživatelské prostředí pro konfiguraci a sledování procesu elektronické faktury pro všechny země nebo regiony
- Rychlejší, snazší a levnější přijetí doplňkových řešení elektronické fakturace v nových zemích nebo regionech
- Konfigurace služby prostřednictvím služby Regulatory Configuration Service (RCS) a globalizace
- Transformace obchodních dat do více formátů elektronických faktur (XML, JavaScript Object Notation \[JSON\], TXT a hodnoty oddělené čárkami \[CSV\]) pomocí konfigurací definovaných v RCS:

    - Formáty elektronických sestav, které jsou k dispozici pro země nebo oblasti, kde není k dispozici konfigurovatelnost pro transformaci e-faktur

- Konfigurovatelné odesílání elektronických faktur externím webovým službám, včetně zpracování certifikace prostřednictvím digitálních podpisů:

    - Integrovaná, snadno rozšiřitelná a konfigurovatelná integrace s dalším obsahem pro několik zemí

    > [!NOTE]
    > V současné době je podporován omezený počet přímých odeslání. Více informací naleznete v předchozích části [Dostupnost](#availability) v tomto tématu. Podpora bude v budoucnu rozšířena.

- Zpracování odpovědí z webových služeb, včetně konfigurovatelného zpracování zpráv o výjimkách
- Podpora elektronických podpisů (například pomocí podpisového algoritmu XMLDSig)
- Hromadné zpracování zpráv elektronické faktury

## <a name="architecture-and-data-flow"></a>Architektura a tok dat

Když je doplněk elektronické fakturace nainstalován z LCS a požadované nastavení je dokončeno ve všech požadovaných aplikacích, je navázáno zabezpečené připojení. Tato služba je v současné době umístěna v datových centrech ve Spojených státech a Evropě. Proto se umístění služby může lišit od umístění související instance Finance nebo Supply Chain Management. Po dokončení nastavení doplňku pro elektronickou fakturaci a zapnutí integrace se vždy, když se odešle elektronická faktura, do doplňku pro elektronickou fakturaci odešlou kmenová data a transakční data související s konkrétním dokumentem.

> [!NOTE]
> Pokud vaše elektronická faktura nebo jakýkoli jiný dokument obsahuje osobní údaje, ověřte, zda vaše použití této funkce splňuje obecné nařízení o ochraně osobních údajů (GDPR) a další předpisy týkající se přenosu osobních údajů.

### <a name="high-level-description-of-the-data-flow"></a>Popis datového toku na vysoké úrovni

1. Klient odešle do služby kanonický obchodní dokument.
2. Na základě kontextových informací, které jsou přijímány od klienta, služba vybere příslušný tok zpracování.
3. Služba spouští akce zpracování. Tyto akce mohou zahrnovat transformaci obchodního dokumentu na elektronickou fakturu, použití elektronického podpisu a odeslání dokumentu do externí webové služby.
4. Všechny přijaté a zpracované dokumenty jsou uloženy v úložišti Azure Blob zákazníka.
5. Všechny tajné kódy klienta a certifikáty, které byly použity ke zpracování, jsou uloženy v trezoru klíčů Azure zákazníka.
6. Služba poskytuje klientovi na vyžádání informace o stavu zpracování obchodního dokumentu, který byl odeslán.
7. Klient obdrží informace o dokončeném zpracování a zpřístupní všechny informace protokolu. Také zpřístupní dokument, který byl vytvořen nebo přijat během zpracování toku.

Následující obrázek ukazuje, jak data proudí do a z doplňku elektronické fakturace.

![Tok dat pro doplněk Elektronická fakturace](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Povolení a používání Elektronické fakturace může vyžadovat odesílání omezených dat, která zahrnují daňové identifikační číslo organizace. To bude předáno agenturám třetích stran oprávněným daňovými úřady pro účely zasílání elektronických faktur v předdefinovaných formátech požadovaných pro integraci s webovými službami těchto vlád. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.

## <a name="additional-resources"></a>Další prostředky

- [Začněte s doplňkem elektronické fakturace](e-invoicing-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Brazílii](e-invoicing-bra-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Mexiko](e-invoicing-mex-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Itálii](e-invoicing-ita-get-started.md)
- [Nastavení doplňku Elektronická fakturace](e-invoicing-setup.md)
