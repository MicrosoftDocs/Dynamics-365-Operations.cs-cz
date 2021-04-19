---
title: Vytvoření URL adresy stránky
description: V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795684"
---
# <a name="create-a-page-url"></a>Vytvoření URL adresy stránky

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.

Úplná nebo absolutní adresa URL, která odkazuje na stránku na webu, se skládá z různých částí. Například adresa URL `https://www.contoso.com/en-us/contactus` má následující části:

- `https://www.contoso.com` – Protokol HTTP a doména pracoviště.
- `/en-us` – Cesta k jazyku webu.
- `/contactus` – Relativní adresa URL stránky **Kontaktujte nás**. Relativní adresa URL se také nazývá *slug* adresy URL.

Doménu webu a volitelnou cestu k jazyku webu vytvoříte při zřízení webu. Na stránce online obchodů v nastaveních webu můžete přidat další domény a cesty k jazyku webu.

Slug adresy URL stránky existuje jako samostatná entita ve vývojovém prostředí webu. Adresa URL stránky se skládá ze dvou částí: názvu, který představuje slug adresy URL, a ukazatel na stránku buď na vašem webu, nebo na externím webu. Adresu URL stránky lze také nakonfigurovat tak, aby přesměrovala na jinou stránku buď na vašem webu, nebo na externím webu.

## <a name="create-a-page-url"></a>Vytvoření URL adresy stránky

Existují dva způsoby vytvoření adresy URL stránky:

- Automaticky, při vytvoření stránky
- Ručně, ze stránky **Adresy URL**

### <a name="create-a-page-url-when-you-create-a-page"></a>Vytvoření adresy URL stránky při vytvoření stránky

Pokud při vytváření nové stránky zadáte název do pole **Adresa URL**, bude na stránce **Adresy URL** automaticky vytvořena adresa URL stránky odkazující na tuto stránku. Po publikování adresy URL a stránky, na kterou odkazuje, mohou uživatelé webu (vaši zákazníci) získat přístup ke stránce, která je přidružena k dané adrese URL.

> [!NOTE]
> Pokud publikujete adresu URL, aniž byste publikovali stránku, na kterou odkazuje, zobrazí se uživatelům webu Chyba 404 při pokusu o přístup na stránku. Pokud publikujete stránku bez publikování adresy URL, která na ni odkazuje, nelze k této stránce přistupovat pomocí adresy URL.

### <a name="manually-create-a-page-url"></a>Ruční vytvoření adresy URL stránky

Když vytváříte novou stránku, nemusíte zadat její adresu URL. Pokud ponecháte pole adresy URL prázdné, bude stránka vytvořena v nepropojeném stavu. V takovém případě nebudou mít zákazníci přístup na stránku, i když bude publikována. Aby byla stránka přístupná, je nutné ručně vytvořit adresu URL a propojit ji se stránkou.

Chcete-li vytvořit adresu URL stránky ručně, postupujte podle následujících kroků.

1. Na stránce **Adresy URL** zvolte **Nová**.
1. Vyberte stránku webu, které má být přiřazena adresa URL.
1. Zadejte slug adresy URL a poté klikněte na tlačítko **OK**.

V tomto okamžiku se adresa URL nachází ve stavu konceptu. Musí být publikována před tím, než mohou uživatelé webu přistupovat k příslušné stránce.

## <a name="update-a-page-url"></a>Aktualizace adresy URL stránky

Chcete-li aktualizovat cílovou stránku adresy URL, postupujte následujícím způsobem.

1. Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.
1. V podokně vlastností vpravo vyberte tlačítko se třemi tečkami (**...**) vedle pole cílové stránky.
1. V dialogovém okně vyberte jinou stránku a pak vyberte možnost **OK**.
1. Uložte a publikujte adresu URL.

## <a name="redirect-a-page-url"></a>Přesměrování adresy URL stránky

V některých případech můžete požadovat, aby vaši zákazníci při požadavku na konkrétní adresu URL zobrazili jinou stránku. V těchto případech je často nejlepší a nejjednodušší změnit stránku, na kterou adresa URL stránky odkazuje. Je však možné, že máte legitimní důvody k přesměrování požadavků na adresu URL na jinou adresu URL pomocí přesměrování HTTP 301 nebo 3023.

Chcete-li přesměrovat adresu URL na jinou adresu URL, postupujte podle následujících kroků.

1. Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.
1. V podokně vlastností vpravo vyberte vlastnost **Přesměrovat**.
1. Vyberte cíl přesměrování:

    - Chcete-li odkázat na jinou stránku na webu, **vyberte volbu** Interní adresa URL, vyberte tlačítkose třemi tečkami (**...**) a vyberte adresu URL, na kterou chcete přesměrovat.
    - Chcete-li odkázat na stránku na externím webu, vyberte volbu **Externí adresa URL** a poté zadejte úplnou adresu URL pro tuto stránku. Nezapomeňte zadat i protokol. Zadejte například `https://domain.com/new/page`. Pokud již adresa URL přesměrovává na interní adresu URL, je nutné před zadáním externí adresy URL vybrat možnost **Vymazat výběr**.

1. Vyberte typ přesměrování:

    - **Trvalé přesměrování (301)** – Tuto možnost vyberte, pokud víte, že se váš obsah trvale přesouvá a neobnoví se na předchozí adresu URL. Vyhledávací weby přiřadí hodnotu SEO (Search Engine Optimization) adresy URL pro přesměrování adrese URL, na kterou je přesměrovávána a aktualizuje jejich záznam, aby se zobrazila nová adresa URL. 
    - **Dočasné přesměrování (302)** – Tuto možnost vyberte, chcete-li přesměrovat provoz bez aktualizace vyhledávacích webů. Tento přístup se obvykle používá v případě, že se obsah brzy vrátí na předchozí adresu URL.

1. Až budete připraveni provést přesměrování, uložte a publikujte adresu URL.

## <a name="additional-resources"></a>Další zdroje

[Přizpůsobení navigace na webu](customize-site-navigation.md)

[Přidání nové webové stránky](add-new-page.md)

[Konfigurace názvu domény](configure-your-domain-name.md)

[Přidání jazyků na web](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
