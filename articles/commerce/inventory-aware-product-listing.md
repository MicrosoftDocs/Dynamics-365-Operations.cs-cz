---
title: Výpis produktů s ohledem na zásoby
description: Tento článek popisuje, jak mohou organizace nakonfigurovat stránky se seznamem produktů na svém webu elektronického obchodování Microsoft Dynamics 365 Commerce, aby byly s ohledem na zásoby.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473726"
---
# <a name="inventory-aware-product-listing"></a>Výpis produktů s ohledem na zásoby

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak mohou organizace nakonfigurovat stránky se seznamem produktů na svém webu elektronického obchodování Microsoft Dynamics 365 Commerce, aby byly s ohledem na zásoby. Stránky se seznamem produktů zahrnují vstupní stránky kategorií a stránky s výsledky vyhledávání.

Zákazníci obecně očekávají, že web elektronického obchodu bude po celou dobu procházení produktů informován o zásobách, takže se mohou rozhodnout, co dělat, když není produkt na skladě. Kategorie [Knihovna modulu Commerce](starter-kit-overview.md) a moduly výsledků vyhledávání lze konfigurovat tak, aby zahrnovaly data zásob. Tímto způsobem můžete poskytovat následující služby:

- Zobrazit vedle produktů štítky úrovně zásob.
- Skryjte produkty, které nejsou skladem, v seznamu produktů.
- Přesunout produkty, které nejsou skladem, na konec seznamu stránek s výsledky vyhledávání.
- Podporovat filtrování produktů na základě zásob.

Chcete-li povolit tyto funkce, musíte nejprve povolit funkci **Vylepšené zjišťování produktů v elektronickém obchodování s ohledem na zásoby** v Commerce headquarters.

> [!NOTE]
> V Commerce verze 10.0.29 je funkce **Vylepšené zjišťování produktů v elektronického obchodování s ohledem na zásoby** ve výchozím nastavení zapnutá.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Nastavení atributu produktu pro dostupnost zásob

Výpis produktů s ohledem na zásoby používá rámec atributů produktu. Nezbytným předpokladem je vytvoření vyhrazeného atributu produktu pro zachycení údajů o dostupnosti zásob.

K nastavení atributu produktu pro dostupnost zásob v Commerce headquarters postupujte následovně.

1. Přejděte na **Retail a Commerce \> Retail a Commerce IT \> Produkty a zásoby \> Vyplnit atributy produktu úrovní zásob**.
1. V dialogovém okně **Vyplnit atributy produktu úrovní zásob** do pole **Atribut produktu a název typu** zadejte vlastní název pro vyhrazený atribut produktu, který bude vytvořen pro zachycení údajů o zásobách.
1. V poli **Dostupnost zásob na základě** vyberte typ množství, na kterém by měl být založen výpočet úrovně zásob: **Fyzický dostupné** nebo **Celkově dostupné**.
1. Nastavte **Dávkové zpracování** na **Ano**.
1. Vyberte **OK**.

> [!NOTE]
> Pro konzistentní výpočet úrovně zásob napříč stránkami se seznamem produktů na vašem webu elektronického obchodu nezapomeňte vybrat stejnou možnost množství pro pole **Dostupnost zásob na základě** pro úlohu **Vyplnit atributy produktu úrovní zásob** a nastavení **Úroveň zásob na základě** v nástroji tvorby webů Commerce.

Po vytvoření vyhrazeného atributu produktu je dalším krokem konfigurace atributu pro online kanál.

Ke konfiguraci atributu pro online kanál v Commerce headquarters postupujte následovně.

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte online kanál, pro který chcete povolit zobrazování produktů s ohledem na zásoby.
1. Vyberte a otevřete přidruženou skupinu atributů a přidejte do ní nový atribut produktu.
1. Až budete hotovi, přejděte na **Retail a Commerce \> IT Retail a Commerce \> Plán distribuce** a spusťte úlohu **1150** (**Katalog**). Doporučujeme naplánovat tuto úlohu jako dávkový proces, který běží se stejnou frekvencí jako úloha **Naplnit atributy produktu úrovní zásob**.

> [!NOTE]
> Ve verzi Commerce 10.0.26 a dřívějších po přidání atributu produktu dostupnosti zásob do skupiny atributů musíte také vybrat **Nastavit metadata atributu** a poté zapnout možnosti **Zobrazit atribut na kanálu**, **Načítatelné**, **Lze vylepšit** a **Lze se dotázat** pro nový atribut produktu.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Konfigurace chování zobrazení pro produkty, které nejsou skladem, na stránkách se seznamem produktů

Po dokončení všech předchozích konfiguračních kroků budou mít zpřesnění na stránkách kategorií a výsledků vyhledávání možnost filtru založeného na zásobách. Pro každou dlaždici produktu, která se objeví na stránce, se zobrazí popisek úrovně zásob.

Na stránce kategorie a výsledků vyhledávání se zobrazují produkty na hlavní úrovni, nikoli na úrovni varianty produktu. Úroveň zásob, která se zobrazuje vedle každého produktu, je agregovaná úroveň zásob, která je určena úrovní zásob všech variant produktu. Úroveň zásob varianty se vypočítá na základě aktuální zásoby dané varianty ve výchozím skladu online kanálu v Commerce headquarters. Úroveň zásob hlavního produktu má dvě možné hodnoty, které představují stavy na skladě a není na skladě. Hlavní produkt je považován za vyprodaný v případě, že nejsou skladem všechny jeho varianty. Jinak se produkt považuje za skladem. Popisek hodnoty je načten z definice [úrovně zásob](inventory-buffers-levels.md). Pokud není definována žádná úroveň zásob, jsou výchozí štítky **Dostupný** a **Vyprodáno**.

Můžete nakonfigurovat **Nastavení zásob pro stránky se seznamem produktů** v nástroji na tvorbu webu Commerce, abyste mohli řídit, jak kategorie a stránka výsledků vyhledávání zobrazuje produkty, které nejsou skladem. Další informace [Použít nastavení zásob](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
