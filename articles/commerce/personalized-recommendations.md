---
title: Povolení doporučení přizpůsobeného produktu
description: V tomto článku je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283607"
---
# <a name="enable-personalized-recommendations"></a>Povolení přizpůsobených doporučení

[!include [banner](includes/banner.md)]

V tomto článku je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.

V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení). Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě (POS). Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.

## <a name="personalization-prerequisites"></a>Předpoklady přizpůsobení

Před tím, než zpřístupníte individuální doporučení produktu zákazníkům, mějte na paměti, že doporučení k produktům jsou podporována pouze pro uživatele z Commerce, kteří migrovali své úložiště do služby Azure Data Lake Store. Aby mohli zákazníci obdržet přizpůsobená doporučení produktů, musí maloobchodníci [zapnout doporučení produktu](enable-product-recommendations.md).

> [!NOTE]
> Zapnete-li doporučení produktu, bude také zapnuto přizpůsobení. Pokud však přizpůsobení vypnete, nevypnete ostatní typy doporučení produktů.

Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="turn-on-personalization"></a>Zapnutí individuálního nastavení

Chcete-li zapnout přizpůsobení, postupujte následujícím způsobem.

1. V centrále Commerce vyhledejte **Správa funkcí**.
1. Volbou **Vše** zobrazíte seznam dostupných funkcí. 
1. Do vyhledávacího pole zadejte **Doporučení**.
1. Vyberte funkci **Přizpůsobená doporučení produktu**.
1. V podokně vlastností **Přizpůsobená doporučení produktu** vyberte **Ihned povolit**.

![Zapnutí individuálního nastavení.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Po zapnutí přizpůsobení se spustí proces generování seznamu doporučení pro individuální produkt. Je možné, že tyto seznamy budou k dispozici a budou viditelné online a v POS.

## <a name="personalized-lists"></a>Přizpůsobené seznamy

Služba doporučení kromě přizpůsobení stávajících seznamů generovaných počítačem umožňuje přizpůsobení možností zjišťování produktů, a to online i v POS.

Po zapnutí přizpůsobení mohou maloobchodní prodejci zobrazit přizpůsobené seznamy výběrů pro vás online nebo seznamy Doporučení pro zákazníky na terminálech POS. Maloobchodní prodejci mohou také použít přizpůsobení pro stávající seznamy doporučení produktů a poskytovat funkce pro přístup k obecnému nařízení o ochraně osobních údajů (GDPR) pro ověřené uživatele. Pokud vypnete přizpůsobení, vypnete také tyto funkce.

### <a name="online-picks-for-you-lists"></a>Online seznamy výběrů pro vás

Seznam výběrů pro vás je seznam strojového učení umělé inteligence (AI-ML), který ověřenému uživateli ukazuje přizpůsobený seznam navrhovaných produktů. Tento seznam je založen na historii nákupů omnikanálu uživatele. Přizpůsobená doporučení jsou dynamicky aktualizována, protože uživatel provádí více nákupů. Tento typ seznamu také podporuje filtrování kategorií, takže maloobchodní prodejci mohou na základě navigačních hierarchií zobrazit přední výběry.

Dříve než může být seznam výběrů pro vás zobrazen na libovolné stránce elektronického obchodu, musí být splněny následující požadavky uživatele:

- Uživatelé musí být přihlášeni. Anonymní uživatelé neuvidí přizpůsobená doporučení.
- Uživatelé musí mít na svém účtu alespoň jeden nákup.
- Uživatelé musí souhlasit s přijetím individuálních doporučení.

Na následujícím obrázku je znázorněn příklad seznamu výběrů pro vás na stránce online obchodu.

![Seznam Online výběry pro vás.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Seznamy Doporučeno pro zákazníka v POS

Pokud maloobchodní prodejci chtějí vylepšit své zkušenosti se získáváním klientů, mohou přizpůsobit existující stránky podrobností o odběrateli přidáním kontextové části Doporučená pro zákazníka.

Na následujícím obrázku je znázorněn příklad seznamu Doporučeno pro zákazníka na terminálu POS.

![Seznamy Doporučeno pro zákazníka v POS.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Použít přizpůsobení u existujících seznamů doporučení

Maloobchodní prodejci mohou použít přizpůsobení pro stávající seznamy doporučení, jako například nový, vytváření trendů, nejprodávanější, lidem se také líbí a často nakupované společně. Pokud je přizpůsobení použito u existujících seznamů, položky, které byly dříve zakoupeny, jsou z těchto seznamů odebrány. Výchozí verze existujících seznamů jsou zobrazeny pro anonymní uživatele i pro uživatele, kteří se odhlásili od příjmu přizpůsobených doporučení. Maloobchodní prodejci proto nemusí ručně udržovat samostatné stránky.

Například přihlášený uživatel již nakoupil černé hodinky a hnědé pracovní boty, které se zobrazují v seznamu Trendy - výchozí na následujícím obrázku. Z toho vyplývá, že se uživateli zobrazí nové produkty místo těchto produktů, jak je uvedeno v seznamu "trendy-přizpůsobení".

![Použití individuálního nastavení.](./media/applypersonalization.png)

Chcete-li použít přizpůsobení pro existující seznam doporučení v modulu Commerce Site Builder, postupujte podle následujících kroků.

1. Otevře existující stránku konfigurátoru webu, která obsahuje modul pro shromažďování produktů.
1. V levém navigačním podokně vyberte modul inkasa produktu.
1. V pravém navigačním podokně v části **Produkty** vyberte seznam.
1. V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte v části **Typ** typ seznamu.
1. Zaškrtněte políčko **Použít přizpůsobení** a vyberte **OK**.

    ![Aplikace přizpůsobení na seznam trendů.](./media/ApplyPersonalizationToTrending.PNG)

1. Uložte fragment stránky, dokončete úpravy a publikujte ji. Po publikování stránky budou přihlášeným uživatelům zobrazeny přizpůsobené seznamy trendů.

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
