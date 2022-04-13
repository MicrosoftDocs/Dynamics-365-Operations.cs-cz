---
title: Kopírování webu elektronického obchodu
description: Toto téma popisuje, jak zkopírovat existující web elektronického obchodu v rámci prostředí elektronického obchodu nebo mezi nimi v konfigurátoru webů Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: a23f544cbd1e960cb704d2b9666b7db4c3894b5e
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462319"
---
# <a name="copy-an-e-commerce-site"></a>Kopírování webu elektronického obchodu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak zkopírovat existující web elektronického obchodu v rámci prostředí elektronického obchodu nebo mezi nimi v konfigurátoru webů Microsoft Dynamics 365 Commerce.

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
1. V podokně akcí zvolte **Kopírovat web**.
1. V dialogovém okně **Kopírovat web** zadejte v poli **Název nového webu** název nového webu. Název nového webu musí být v prostředí elektronického obchodu jedinečný. Pole **Zdrojový klient** a **Zdrojový web** se automaticky vyplní informacemi o aktuálním klientu a vybraném webu.
1. Vyberte příkaz **Vytvořit kopii**.

Po ověření informací se zobrazí upozornění, že byla vytvořena nová úloha kopírování webu. Průběh úlohy můžete sledovat v [pravém podokně stránky **Úlohy klienta**](#monitor-the-site-copy-operation). Po úspěšném dokončení operace kopírování se nový web zobrazí v seznamu webů v zobrazení seznamu webů.

Následující obrázek ukazuje příklad dialogového okna **Kopírovat web** v konfigurátoru webů.

![Dialogové okno Kopírovat web v konfigurátoru webů.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopírování webu mezi dvěma prostředími elektronického obchodu

Chcete-li zkopírovat web mezi dvěma prostředími elektronického obchodu, postupujte takto.

1. Přihlaste se jako do konfigurátoru webů v cílovém prostředí elektronického obchodu.
1. V podokně akcí zvolte **Kopírovat web**.
1. V dialogovém okně **Kopírovat web** zadejte v poli **Název nového webu** název nového webu. Název nového webu musí být v prostředí elektronického obchodu jedinečný.
1. V poli **Zdrojový klient** vyberte jméno zdrojového klienta.
1. V poli **Zdrojový web** vyberte zdrojový web.
1. Vyberte příkaz **Vytvořit kopii**.

> [!NOTE]
> Oprávnění správce klienta jsou vyžadována ve zdrojovém i cílovém prostředí elektronického obchodu.

Po ověření informací se zobrazí upozornění, že byla vytvořena nová úloha kopírování webu. Průběh úlohy můžete sledovat v [pravém podokně stránky **Úlohy klienta**](#monitor-the-site-copy-operation). Po úspěšném dokončení operace kopírování se nový web zobrazí v seznamu webů v zobrazení seznamu webů.

## <a name="monitor-the-site-copy-operation"></a>Sledování operace kopírování webu

Chcete-li sledovat průběh operace kopírování webu, postupujte takto.

1. Přihlaste se jako do konfigurátoru webů v cílovém prostředí elektronického obchodu.
1. V levém podokně vyberte položku **Úlohy klienta**.
1. Na stránce **Úlohy klienta** vyhledejte a vyberte v seznamu úlohu kopírování webu. Vpravo se zobrazí podokno ukazující stav a podrobnosti vybrané úlohy.

Úlohu, která má stav **Probíhá**, můžete zrušit. Vyberte úlohu v seznamu a poté vyberte v podokně akcí příkaz **Zrušit**.

Můžete znovu zkusit provést úlohu, která má stav **Neúspěšné** nebo **Dokončeno s chybami**. Vyberte úlohu v seznamu a poté vyberte v podokně akcí příkaz **Opakovat**.

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
