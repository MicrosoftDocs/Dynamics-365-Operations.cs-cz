---
title: Konfigurace nastavení e-mailu v Microsoft Dynamics 365 Talent - Attract
description: V tomto tématu je vysvětleno, jak nakonfigurovat nastavení e-mailu odeslaného v aplikaci Microsoft Dynamcis 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a457deec757a5d5a3e01c6903b2dd7a9d975ef0b
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551534"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-talent---attract"></a>Konfigurace nastavení e-mailu v Microsoft Dynamics 365 Talent - Attract

[!include[banner](../includes/banner.md)]

Vaše značka vytváří vztah důvěryhodnosti a pomůže vám vytvořit vztah s uchazeči ještě než zažádají o pozice u vás. Pozitivní vnímání značky přitahuje nejlepší talenty a zvyšuje loajalitu stávajících zaměstnanců. Microsoft Dynamics 365 Talent: Attract umožňuje konfigurovat e-maily tak, aby odrážely značku vaší společnosti. Proto můžete poskytnout konzistentní zkušenosti uchazečům o práci při procházení procesu žádosti.

Attract umožňuje provést následující akce:

- Konfigurace nastavení e-mailu tak, aby byl použit účet e-mailové služby Microsoft Exchange společnosti. Tímto způsobem uchazeči ví, že e-maily přicházejí z vaší společnosti. Můžete například nakonfigurovat nastavení tak, aby uchazeči dostávali e-maily z adresy `recruiting@contoso.com` místo z adresy `contoso@microsoft.com`.
- Vytvořte konzistentní uvádění značky ve veškeré e-mailové komunikaci nastavením globálního záhlaví a zápatí pro všechny e-mailové šablony. 

> [!NOTE]
> Chcete-li nastavit Attract tak, aby pro odesílání e-mailů používal účet e-mailové služby vaší společnosti, potřebujete doplněk Comprehensive hiring.

## <a name="connect-an-email-service-account"></a>Propojení účtu e-mailové služby

Připojením e-mailového účtu vaší společnosti můžete vytvořit e-mailové prostředí s informacemi o vašich uchazečích o zaměstnání. Pokud účet společnosti nepřipojíte, Attract použije výchozí účet e-mailové služby společnosti Microsoft.

1. Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.
2. Na kartě **Nastavení e-mailu** v části **Účty e-mailové služby** vyberte možnost **Připojit účet společnosti**.

    ![Připojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-email-service-accounts.png)

    Další informace o postupu při vytváření sdíleného e-mailového účtu naleznete v tématu [Sdílené poštovní schránky v aplikaci Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. V přihlašovacím okně společnosti Microsoft se přihlaste pomocí svých podnikových přihlašovacích údajů.
4. Pokud jste ještě nenastavili účet e-mailové služby nebo pokud chcete přidat nový, vyberte možnost **Přidat nový účet služby** a pak zadejte své e-mailové informace. Pokud jste již nastavili účet e-mailové služby, který chcete použít, vyberte jej.

Po úspěšné konfiguraci účtu e-mailové služby se tento účet zobrazí v části **Účty e-mailové služby**.

## <a name="disconnect-an-email-service-account"></a>Odpojení účtu e-mailové služby

Chcete-li přestat používat doménu společnosti v e-mailové komunikaci prostřednictvím aplikace Attract, můžete odpojit účet e-mailové služby.

1. Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.
2. Na kartě **Nastavení e-mailu** vyberte v části **Účty e-mailové služby** tlačítko **Další** (tři svislé tečky) vedle účtu e-mailové služby, který chcete odpojit.
3. Vyberte **Odpojit e-mailový účet**.

    ![Odpojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-disconnect-email-account.png)

4. Po zobrazení výzvy k potvrzení operace vyberte možnost **Odpojit.**

    ![Potvrzení odpojení účtu e-mailové služby společnosti v aplikaci Attract](./media/attract-admin-email-confirm-disconnect.png)

Pokud nepřipojíte jiný účet e-mailové služby, budou e-maily odeslané z aplikace Attract používat výchozí e-mailovou službu se značkou Microsoft.

## <a name="configure-email-template-settings"></a>Konfigurace nastavení šablony

Můžete odeslat obrázek loga společnosti a další informace jako značku pro vaše e-mailové zprávy. Můžete také poskytnout odkazy na zásady ochrany osobních údajů a podmínky použití v zápatích e-mailů.

> [!NOTE]
> Musíte dodržovat platné zákony vaší země nebo oblasti a také země nebo oblasti, které se vztahují na příjemce e-mailu. Tyto zákony zahrnují předpisy o ochraně proti nevyžádané poště.

1. Zvolte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.
2. Na kartě **Nastavení e-mailu** ve skupinovém rámečku **nastavení šablony e-mailu** přetáhněte obrázek, který chcete použít jako záhlaví e-mailu, do pole s obrázkem, nebo klepnutím na tlačítko v poli obrázek vyhledejte soubor. Chcete-li nahradit existující obrázek, musíte nejprve vybrat **odebrat** vedle obrázku. Obraz musí být soubor JPEG, JPG, PNG nebo SVG. Doporučená velikost pro obrázky je mezi 25 a 800 pixelů široká a mezi 25 a 150 pixely vysoká. Maximální velikost souboru pro záhlaví je 1 megabajt (MB).

    ![Přidání obrázku pro záhlaví e-mailu vaší společnosti](./media/attract-admin-email-header.png)

3. V části **Zásady ochrany osobních údajů pro komunikace** uveďte odkaz na zásady ochrany osobních údajů společnosti. V části **Podmínky pro komunikaci** zadejte odkaz na podmínky použití ve vaší společnosti.

    ![Přidání odkazů na zásady ochrany osobních údajů společnosti a podmínky použití zápatí e-mailu](./media/attract-admin-email-footer.png)

4. Výběrem možnosti **Uložit** uložte nastavení šablony e-mailu.
