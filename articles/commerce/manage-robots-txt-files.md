---
title: Správa souborů robots.txt
description: Tento článek popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: b66d6f725c345ff82d3f3f8c33d609fa770addf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286404"
---
# <a name="manage-robotstxt-files"></a>Správa souborů robots.txt

[!include [banner](includes/banner.md)]

Tento článek popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.

Protokol pro zakázání přístupu robotům, neboli robots.txt, je standardem, který weby používají ke komunikaci s webovými roboty. Protokol dává pokyny webovým robotům o všech oblastech webu, které by neměly být navštíveny. Roboti často používají vyhledávací stroje k indexování webů.

Chcete-li ze serveru vyloučit roboty, vytvoříte na serveru soubor. V tomto souboru určíte zásady přístupu pro roboty. Soubor musí být přístupný prostřednictvím protokolu HTTP na místní adrese URL **/robots.txt**. Soubor robots.txt pomáhá vyhledávacím webům indexovat obsah vašeho webu.

Dynamics 365 Commerce umožňuje odeslat do vaší domény soubor robots.txt. Pro každou doménu v prostředí Commerce můžete odeslat jeden soubor robots.txt a přidružit jej k této doméně.

Další informace o souboru robots.txt naleznete v části [Stránky webových robotů](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Odeslání souboru robots.txt

Po vytvoření a úpravě souboru robots.txt podle [protokolu pro zakázání přístupu robotům](https://www.robotstxt.org/orig.html) zkontrolujte, zda je soubor přístupný v počítači, ve kterém budete používat vývojářské nástroje Commerce. Soubor musí mít název **robots.txt**. Pro dosažení optimálních výsledků musí být ve formátu uvedeném v protokolu. Každý zákazník Commerce je zodpovědný za ověřování a údržbu obsahu souboru robots.txt. Chcete-li odeslat soubor robots.txt, musíte být přihlášen ke Commerce jako správce systému.

Postup odeslání souboru robots.txt v Commerce je následovný.

1. Přihlaste se k Commerce jako správce systému.
2. V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.
3. V části **Nastavení klienta** vyberte **Robots.txt**. V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.
4. Volbou **Spravovat** odešlete soubor robots.txt do domény ve vašem prostředí.
5. V nabídce vpravo klikněte na tlačítko **Odeslat** (šipka směřující nahoru) vedle domény, která je přidružena k souboru robots.txt. Zobrazí se dialogové okno prohlížeče souborů.
6. V dialogovém okně vyhledejte a vyberte soubor robots.txt, který chcete odeslat pro přidruženou doménu, a pak volbou **Otevřít** dokončete odeslání souboru.

> [!NOTE] 
> Během odesílání Commerce ověří, že soubor je textový soubor, ale neověří obsah souboru.

## <a name="download-a-robotstxt-file"></a>Stažení souboru robots.txt

Postup stažení souboru robots.txt v Commerce je následovný.

1. Přihlaste se k Commerce jako správce systému.
2. V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.
3. V části **Nastavení klienta** vyberte **Robots.txt**. V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.
4. Volbou **Spravovat** stáhnete soubor robots.txt do domény ve vašem prostředí.
5. V nabídce vpravo klikněte na tlačítko **Stáhnout** (šipka směřující dolů) vedle domény, která je přidružena k souboru robots.txt. Zobrazí se dialogové okno prohlížeče souborů.
6. V dialogovém okně přejděte k požadovanému umístění na místním disku, potvrďte nebo zadejte název souboru a potom volbou **Uložit** dokončete stahování.

> [!NOTE]
> Tento postup lze použít ke stažení pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.

## <a name="delete-a-robotstxt-file"></a>Odstranění souboru robots.txt

Postup odstranění souboru robots.txt v Commerce je následovný.

1. Přihlaste se k Commerce jako správce systému.
2. V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.
3. V části **Nastavení klienta** vyberte **Robots.txt**. V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.
4. Volbou **Spravovat** odstraníte soubor robots.txt do domény ve vašem prostředí.
5. V nabídce vpravo klikněte na tlačítko **Odstranit** (symbol odpadkového koše) vedle domény, která je přidružena k souboru robots.txt. Zobrazí se okno prohlížeče souborů.
6. V okně prohlížeče souborů vyhledejte a vyberte soubor robots.txt, který chcete odstranit pro danou doménu, a vyberte volbu **Otevřít**. Zobrazí se okno se zprávou upozornění.
7. V okně se zprávou vyberte možnost **Odstranit** a potvrďte odstranění souboru robots.txt.

> [!NOTE] 
> Tento postup lze použít k odstranění pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
