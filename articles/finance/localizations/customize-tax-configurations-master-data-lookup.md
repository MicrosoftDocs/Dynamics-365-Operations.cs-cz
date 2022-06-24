---
title: Přizpůsobení konfigurací daní pro vyhledávání hlavních dat
description: Tento článek vysvětluje, jak přizpůsobit konfigurace daní za účelem rozšíření funkcí vyhledávání kmenových dat.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 31c15c47fa1dc6861ff555a991d5f9233b7df35e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845177"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Přizpůsobení konfigurací daní pro vyhledávání hlavních dat

[!include [banner](../includes/banner.md)]

Postupujte podle kroků v tomto článku pro přizpůsobení konfigurací daní za účelem rozšíření funkcí vyhledávání kmenových dat.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Import konfigurace daně poskytnuté společností Microsoft

1. V Regulatory Configuration Service (RCS), v pracovním prostoru **Elektronické hlášení** vyberte poskytovatele konfigurace **Microsoft**.
2. Vyberte **Úložiště**.
3. Vyberte **Globální** a potom vyberte **Otevřít**.
4. Vyberte konfiguraci daně, např. **Konfigurace výpočtu daně** a poté na kartě **Verze** vyberte verzi.
5. Vyberte **Import**.

> [!NOTE]
> Ve výchozím nastavení je importováno mapování modelu Dataverse. Pokud se během procesu importu konfigurace zobrazí varovné zprávy, povolte virtuální entity v Dataverse. Další informace viz [Povolení virtuálních entit Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Vytvoření přizpůsobené konfigurace datového modelu

1. V pracovním prostoru **Elektronické hlášení** vyberte **Daňové konfigurace** a poté vyberte konfiguraci datového modelu, kterou chcete rozšířit. Například vyberte **Datový model výpočtu daně**.
2. Vyberte **Vytvořit konfiguraci**.
3. Vyberte **Model zdanitelného dokladu odvozený z Název: Datový model výpočtu daně, Microsoft**.
4. V poli **Název** zadejte **Datový model přizpůsobení**.
5. Vyberte **Vytvořit konfiguraci**.

## <a name="create-customized-reference-models"></a>Vytváření přizpůsobených referenčních modelů

1. Na stránce **Daňové konfigurace** vyberte **Přizpůsobení datového modelu** a poté vyberte **Návrhář**.
2. Vyberte tlačítko se třemi tečkami (**…**) poté vyberte zobrazení **Referenční model**.

    [![Referenční model.](./media/pic2.png)](./media/pic2.png)

3. Vytvořte přizpůsobený referenční model. Přizpůsobený model je kořenový model. Přizpůsobená entita je seznam záznamů. Přizpůsobené pole je pole řetězce, které chcete použít při vyhledávání. V případě potřeby můžete přidat další pole.
4. Vyberte tlačítko se třemi tečkami (**…**) poté vyberte zobrazení **Zdanitelný doklad**.
5. Vyberte atribut, který se má svázat s přizpůsobeným referenčním modelem. Například vyberte **Přizpůsobený atribut** a poté postupujte takto:

    1. Vyberte **Vybrat referenční model**.
    2. Vyberte **Přizpůsobený model** a poté vyberte **OK**. Název referenčního modelu se aktualizuje na hodnotu pole **Přirozený klíč**.

        [![Dialogové okno Vybrat referenční model.](./media/pic5.png)](./media/pic5.png)

    3. Vyberte **Uložit** a potom **Dokončit**.

## <a name="create-a-customized-model-mapping-configuration"></a>Vytvoření přizpůsobené konfigurace mapování modelu

1. V pracovním prostoru **Elektronické hlášení** vyberte **Daňové konfigurace** a poté vyberte konfiguraci **Mapování modelu Dataverse**.
2. V poli **Výchozí pro pole mapování modelu** vyberte **Ne**.
3. Vyberte **Vytvořit konfiguraci**.
4. Vyberte **Mapování modelu zdanitelného dokladu odvozený z Název: Model mapování Dataverse, Microsoft**.
5. V poli **Název** zadejte **Mapování modelu přizpůsobení**.
6. V poli **Cílový model** vyberte datový model **Datový model přizpůsobení**.
7. Vyberte **Vytvořit konfiguraci**.

    [![Dialogové okno Vytvořit konfiguraci – rozevírací seznam.](./media/pic6.png)](./media/pic6.png)

8. Vyberte **Mapování modelu přizpůsobení** a nastavte pole **Připojená aplikace** k připojení, které bylo vytvořeno v kroku 8 v [Nastavení prostředí pro vyhledávání kmenových dat](tax-service-set-up-environment-master-data-lookup.md).
9. Nastavte pole **Výchozí pro mapování modelu** na **Ano**.

## <a name="create-customized-model-mappings"></a>Vytvoření přizpůsobených mapování modelů

1. Na stránce **Daňové konfigurace** vyberte **Mapování modelu přizpůsobení**.
2. Vyberte **Návrhář** a poté vyberte **Model přizpůsobení**.

    [![Model přizpůsobení.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Mapování modelu na entitu Dataverse

1. Na stránce **Návrhář mapování modelu** vyberte **Model přizpůsobení** a poté vyberte **Návrhář**.
2. Ve stromě **Typy zdrojů dat** vyberte **Tabulka Dataverse**.
3. Na kartě **Zdroje dat** vyberte **Přidat kořen**.
4. Do pole **Název** zadejte **Přizpůsobené Dataverse**.
5. Ve druhém poli **Název** vyberte entitu.
6. Vyberte **OK**.

    [![Dialogové okno vlastnosti zdroje dat „Tabulka“.](./media/pic9.png)](./media/pic9.png)

7. Vyberte **Přizpůsobené Dataverse** a **Přizpůsobená entita** a poté vyberte **Svázat**.

    [![Přizpůsobené Dataverse a přizpůsobená vazba entity.](./media/pic10.png)](./media/pic10.png)

8. V části **Přizpůsobené Dataverse** a **Přizpůsobené pole** vyberte pole a poté vyberte **Svázat**.

    [![Přizpůsobené Dataverse a přizpůsobená vazba pole.](./media/pic11.png)](./media/pic11.png)

9. Vyberte **Uložit** a potom **Dokončit**.

## <a name="create-a-customized-tax-configuration"></a>Vytvoření přizpůsobené daňové konfigurace

1. V pracovním prostoru **Elektronické hlášení** vyberte **Daňové konfigurace** a poté vyberte **Konfigurace výpočtu daně**.
2. Vyberte **Vytvořit konfiguraci**.
3. Vyberte **Konfigurace daňové služby odvozená z Název: Konfigurace výpočtu daně, Microsoft**.
4. V poli **Název** zadejte **Konfigurace přizpůsobení**.
5. Vyberte **Vytvořit konfiguraci**.
6. Vyberte **Konfigurace přizpůsobení** a poté vyberte **Návrhář**.
7. V poli **Datový model** vyberte **Přizpůsobení datového modelu**.
8. V poli **Verze datového modelu** vyberte odpovídající verzi datového modelu.

    [![Část vlastnosti.](./media/pic13.png)](./media/pic13.png)

9. Zvolte **Dokončit**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
