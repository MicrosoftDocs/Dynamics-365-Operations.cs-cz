---
title: Začínáme se službou nákladového účetnictví (privátní verze Preview)
description: V tomto tématu jsou uvedeny podrobné informace o licencích a pokyny k instalaci služby nákladového účetnictví.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bbf2df112657342245aca2bd02e06cee7e51ea82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251043"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Začínáme se službou nákladového účetnictví (privátní verze Preview)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Tato funkce popsaná v tomto tématu je k dispozici jako součást soukromé verze Preview. Obsah tohoto tématu a funkce, které popisuje, se mohou změnit. Další informace o předchozích verzích naleznete v tématu [Často kladené dotazy k aktualizacím služby One Version](../../fin-ops-core/fin-ops/get-started/one-version.md).

Služba nákladového účetnictví umožňuje provádět účetnictví pro více skladů ve vámi vytvořených hlavních knihách nákladového účetnictví. Jednotlivé hlavní knihy nákladového účetnictví se přidružují ke *konvencím*. Konvence je kolekce následujících typů zásad účetnictví:

- Objekt nákladů
- Základ pro měření vstupu
- Předpoklad toku nákladů
- Prvek nákladů

> [!NOTE]
> I po zapnutí služby nákladového účetnictví můžete v systému Microsoft Dynamics 365 Supply Chain Management stále provádět skladové účetnictví obvyklým způsobem.

Služba nákladového účetnictví je doplněk. Chcete-li zpřístupnit její funkce, musíte ji nainstalovat z Microsoft Dynamics Lifecycle Services (LCS). Proto ji můžete vyhodnotit v testovacím prostředí před tím, než ji zapnete v provozním prostředí.

Služba nákladového účetnictví aktuálně nepodporuje všechny funkce správy nákladů, které jsou integrovány v aplikaci Dynamics 365 Supply Chain Management. Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici, bude vyhovovat vašim požadavkům.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Jak získat službu nákladového účetnictví (privátní verze Preview)

> [!IMPORTANT]
> Chcete-li použít službu nákladového účetnictví, je nutné mít prostředí LCS s vysokou dostupností (nikoli prostředí OneBox) a musíte používat Dynamics 365 Supply Chain Management verze 10.0.11 nebo novější.

Chcete-li se zaregistrovat do privátní verze Preview služby nákladového účetnictví, zašlete prosím své ID prostředí LCS e-mailem do [služby nákladového účetnictví (privátní verze Preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Po vašem schválení pro program vám pošleme e-mail, který obsahuje klíč beta pro službu nákladového účetnictví. Po přijetí klíče beta můžete pokračovat [instalací doplňku](#install).

## <a name="licensing"></a>Licence

Služba nákladového účetnictví je licencována společně se standardními funkcemi skladového účetnictví, které jsou k dispozici pro řešení Supply Chain Management. Chcete-li používat službu nákladového účetnictví, nemusíte kupovat další licenci.

## <a name="install-the-add-in"></a><a name="install"></a>Instalace doplňku

Chcete-li použít službu nákladového účetnictví, nainstalujte doplněk služby nákladového účetnictví pro Supply Chain Management, jak je popsáno v následujícím postupu.

1. [Zaregistrujte se](#sign-up) pro službu nákladového účetnictví (privátní verze Preview).

1. Přihlaste se do LCS.

1. Přejděte na **Správu funkcí Preview**.

1. Vyberte znaménko plus (**+**).

1. Do pole **Kód** zadejte pro službu nákladového účetnictví svůj beta klíč pro doplněk. (Váš klíč by měl být doručen e-mailem.)

1. Vyberte **Odblokovat**.

1. Otevřete prostředí LCS, do kterého chcete službu přidat.

1. Přejděte na **Úplné podrobnosti**.

1. Přejděte na záložku s náhledem **Doplňky prostředí**.

1. Vyberte možnost **Nainstalovat nový doplněk**.

1. Vyberte **Služba nákladového účetnictví**.

1. Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.

1. Vyberte **Instalovat**.

1. Na záložce s náhledem **Doplňky prostředí** byste měli vidět, že je instalována služba nákladového účetnictví. Po několika minutách by se stav měl změnit z **Probíhá instalace** na **Nainstalováno**. (Tato změna se může projevit až po aktualizaci stránky.) V tomto okamžiku je služba nákladového účetnictví připravena k použití.

## <a name="set-up-the-integration"></a>Nastavení integrace

Chcete-li nastavit integraci mezi službou nákladového účetnictví a Dynamics 365 Supply Chain Management:

1. Přejděte do nabídky **Správa systému > Správa funkcí**.

1. Vyberte možnost **Zkontrolovat aktualizace**.

1. Otevřete kartu **Vše** a vyhledejte funkci nazvanou *Služba nákladového účetnictví*.

1. Vyberte **Povolit**.

1. Přejděte do nabídky **Nákladové účetnictví > Služba nákladového účetnictví > Nastavení > Parametry služby nákladového účetnictví > Parametry integrace**.

1. V poli **ID aplikace** zadejte následující kód:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Do pole **Koncový bod datové služby** zadejte následující adresu URL:<br>https://operationsdataservice.operations365.dynamics.com/

1. Do pole **Koncový bod nákladového účetnictví** zadejte následující adresu URL:<br>https://costaccountingservice.operations365.dynamics.com/

1. Služba nákladového účetnictví je nyní připravena k použití.

## <a name="related-resources"></a>Související prostředky

[Domovská stránka služby nákladového účetnictví](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]