---
title: Kopírování webu elektronického obchodu
description: Tento článek popisuje, jak zkopírovat existující web elektronického obchodu v rámci prostředí elektronického obchodu nebo mezi nimi v konfigurátoru webů Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 9b74e0d48be29272b893c855c229e4003f0c161e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276280"
---
# <a name="copy-an-e-commerce-site"></a>Kopírování webu elektronického obchodu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak zkopírovat existující web elektronického obchodu v rámci prostředí elektronického obchodu nebo mezi nimi v konfigurátoru webů Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce podporuje kopírování nebo klonování webů jako samoobslužnou operaci v konfigurátoru webů Commerce. Weby lze kopírovat v rámci jednoho prostředí elektronického obchodu nebo mezi dvěma prostředími elektronického obchodu. Uživatel, který zahájí operaci kopírování webu, musí být správcem klienta ve zdrojovém i cílovém prostředí elektronického obchodu.

Operace kopírování webu zkopíruje veškerý obsah elektronického obchodu ze zdrojového webu. Tento obsah zahrnuje stránky, fragmenty, šablony, adresy URL a digitální materiály. Než bude možné nový web použít, musí být inicializován prostřednictvím procesu prvního spuštění (FRE). Kanály lze mapovat a spravovat v konfigurátoru webů v nabídce **Nastavení webu \> Kanály**.

Doba trvání operace kopírování webu závisí především na počtu digitálních materiálů na zdrojovém webu. U výjimečně velkých webů doporučujeme raději zvážit operaci kopírování prostředí. (Tato operace je známá také jako operace přenositelnosti dat).

> [!NOTE]
> - Zdrojový web bude po dobu operace kopírování webu možné pouze číst.
> - Kopírují se pouze publikované verze dokumentů. Pokud nebyly publikovány žádné verze, zkopírují se pouze nejnovější verze.
> - Historie verzí obsahu nebude na cílovém webu k dispozici.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Kopírování webu v prostředí elektronického obchodu

Chcete-li zkopírovat web v prostředí elektronického obchodu, postupujte takto.

1. Přihlaste se do konfigurátoru webů pro prostředí, kde chcete provést operaci kopírování.
1. Otevřete zobrazení seznamu webů výběrem položky **Přepínač webů** v pravém horním rohu a poté vyberte **Spravovat weby**.
1. Vyhledejte web, který chcete zkopírovat nebo klonovat, a vyberte ho zaškrtnutím políčka vedle názvu webu.
1. Na příkazovém řádku vyberte možnost **Kopírovat web**.
1. V rozbalovací nabídce **Kopírovat web** zadejte v poli **Název nového webu** název nového webu. Název nového webu musí být v prostředí elektronického obchodu jedinečný. Pole **Zdrojový klient** a **Zdrojový web** se automaticky vyplní informacemi o aktuálním klientu a vybraném webu.
1. Vyberte příkaz **Vytvořit kopii**.

Po ověření informací se zobrazí upozornění, že byla vytvořena nová úloha kopírování webu. Průběh úlohy můžete sledovat v [pravém podokně stránky **Úlohy klienta**](#monitor-the-site-copy-operation). Po úspěšném dokončení operace kopírování se nový web zobrazí v seznamu webů v zobrazení seznamu webů.

Následující obrázek ukazuje příklad rozbalovací nabídky **Kopírovat web** v konfigurátoru webů.

![Rozbalovací nabídka Kopírovat web v konfigurátoru webů.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopírování webu mezi dvěma prostředími elektronického obchodu

Chcete-li zkopírovat web mezi dvěma prostředími elektronického obchodu, postupujte takto.

1. Přihlaste se jako do konfigurátoru webů v cílovém prostředí elektronického obchodu.
1. Na příkazovém řádku vyberte možnost **Kopírovat web**.
1. V rozbalovací nabídce **Kopírovat web** zadejte v poli **Název nového webu** název nového webu. Název nového webu musí být v prostředí elektronického obchodu jedinečný.
1. V poli **Zdrojový klient** vyberte jméno zdrojového klienta.
1. V poli **Zdrojový web** vyberte zdrojový web.
1. Vyberte příkaz **Vytvořit kopii**.

> [!NOTE]
> Oprávnění správce klienta jsou vyžadována ve zdrojovém i cílovém prostředí elektronického obchodu.

Po ověření informací se zobrazí upozornění, že byla vytvořena nová úloha kopírování webu. Průběh úlohy můžete sledovat v [pravém podokně stránky **Úlohy klienta**](#monitor-the-site-copy-operation). Po úspěšném dokončení operace kopírování se nový web zobrazí v seznamu webů v zobrazení seznamu webů.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Mapovat kanály během operace kopírování webu (volitelné)

Zdrojové kanály a národní prostředí lze mapovat na cílové kanály a národní prostředí jako součást operace kopírování webu. Pokud je mapování kanálů provedeno jako součást operace kopírování webu, není vyžadována inicializace webu pomocí procesu FRE a konfigurace kanálů v nastavení webu. 

Chcete-li namapovat všechny kanály a národní prostředí „tak, jak jsou“ (1 : 1) v nástroji pro tvorbu webu, postupujte takto.

1. Otevřete zobrazení seznamu webů výběrem položky **Přepínač webů** v pravém horním rohu a poté vyberte **Spravovat weby**.
1. Vyhledejte web, který chcete zkopírovat nebo klonovat, a vyberte ho zaškrtnutím políčka vedle názvu webu.
1. Na příkazovém řádku vyberte možnost **Kopírovat web**.
1. V rozbalovací nabídce **Kopírovat web** zadejte hodnoty pro **Název nového webu**, **Zdrojový tenant** a **Zdrojový web** (pokud již není přítomen).
1. Vyberte **Přidat mapování kanálu**.
1. V rozbalovací nabídce **Nakonfigurovat kanály a národní prostředí webu** vyberte **Zdrojový kanál** a poté vyberte zdrojový kanál.  
1. Vyberte **Cílový kanál** a poté vyberte stejný kanál jako zdrojový kanál. 
1. Vyberte **Přidat národní prostředí**.
1. Vyberte **Zdrojové národní prostředí** a poté vyberte zdrojové národní prostředí.
1. Vyberte **Cílové národní prostředí** a poté vyberte stejné národní prostředí jako zdrojové národní prostředí. 
1. Jako **Cesta adresy URL** zadejte jedinečnou cestu URL, která se aktuálně v cílovém prostředí nepoužívá.
1. Opakujte kroky 8–11 pro každé národní prostředí, které má být mapováno pro kanál.
1. Zvolte **Použít**.
1. Opakujte kroky 6 až 11 pro každý zdrojový kanál.
1. Vyberte **Zavřít**.
1. Zkontrolujte přesnost konfigurace a poté vyberte **Kopírovat web**.

> [!NOTE]
> Všechny zdrojové kanály a národní prostředí musí být namapovány a lze je namapovat pouze jednou.

## <a name="monitor-the-site-copy-operation"></a>Sledování operace kopírování webu

Chcete-li sledovat průběh operace kopírování webu, postupujte takto.

1. Přihlaste se jako do konfigurátoru webů v cílovém prostředí elektronického obchodu.
1. V levém podokně vyberte položku **Úlohy klienta**.
1. Na stránce **Úlohy klienta** vyhledejte a vyberte v seznamu úlohu kopírování webu. Vpravo se zobrazí podokno ukazující stav a podrobnosti vybrané úlohy.

Úlohu, která má stav **Probíhá**, můžete zrušit. Vyberte úlohu v seznamu a poté vyberte na panelu příkazů vyberte **Zrušit**.

Můžete znovu zkusit provést úlohu, která má stav **Neúspěšné** nebo **Dokončeno s chybami**. Vyberte úlohu v seznamu a poté vyberte na panelu příkazů **Opakovat**.

> [!NOTE]
> Zpracování videosouborů může pokračovat po dokončení úlohy kopírování webu.

Následující obrázek ukazuje příklad pravého podokna stránky **Úlohy klienta** v konfigurátoru webů.

![Podrobnosti úlohy v pravém podokně stránky Úlohy klienta v konfigurátoru webů.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Inicializace nového webu pomocí procesu FRE

Než bude možné nový web použít, musí být inicializován prostřednictvím procesu FRE.

Chcete-li inicializovat nový web pomocí procesu FRE, postupujte takto.

1. Přihlaste se do konfigurátoru webů pro nový web.
1. Otevřete zobrazení seznamu webů výběrem položky **Přepínač webů** v pravém horním rohu a poté vyberte **Spravovat weby**.
1. Najděte a vyberte nový web, který chcete inicializovat.
1. V dialogu **Nastavte svůj web** vyberte doménu v poli **Vybrat doménu**. Vybírat můžete ze všech domén, které byly přidruženy k prostředí elektronického obchodu během inicializace.
1. V poli **Vyberte výchozí kanál** vyberte přidružený online kanál obchodu. Zvolený kanál bude poskytovat sortimenty a další informace, které jsou uloženy v centrále Commerce.
1. V poli **Vyberte výchozí jazyk** vyberte výchozí jazyk pro vytváření. Vybírat můžete ze všech jazyků, které byly konfigurovány pro vybraný kanál internetového obchodu.
1. Hodnota pole **Cesta** se skládá ze základní domény a volitelné cesty URL, kterou můžete zadat. Cestu URL můžete ponechat prázdnou, pokud bude kanál obsluhován z kořenového adresáře domény, nebo pokud tyto informace chcete zadat později v zobrazení konfigurace kanálu v konfigurátoru webů. Cesta webu musí být v prostředí elektronického obchodu jedinečná.
1. Vyberte **OK**. Web se inicializuje pomocí vámi zadaných údajů a znovu se zobrazí zobrazení pro správu webu.

Následující obrázek ukazuje příklad dialogového okna **Nastavte svůj web** v konfigurátoru webů.

![Dialogové okno Nastavte svůj web v konfigurátoru webů.](media/site-copy_3.png)

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-b2c-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
