---
title: Машинное обучениеное обучение GPU с ускорением в подсистеме Windows для Linux
description: Дополнительные сведения о поддержке WSL 2 для NVIDIA CUDA, Директмл, Tensorflow и PyTorch.
keywords: WSL, Windows, подсистема Windows, вычисление GPU, ускорение GPU, NVIDIA, CUDA, Директмл, Tensorflow, PyTorch, NVIDIA CUDA Preview, драйвер GPU, Инструментарий NVIDIA Container, Docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f101022dec534055905b25619a6c4fcee36f3f7d
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "84947418"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a><span data-ttu-id="d6b2c-104">Обучение производительности GPU с ускорением машинного обучения в подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="d6b2c-104">GPU accelerated machine learning training in the Windows Subsystem for Linux</span></span>

<span data-ttu-id="d6b2c-105">Поддержка вычислений GPU, #1 наиболее востребованной функции WSL теперь доступна для предварительного просмотра с помощью программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b2c-105">Support for GPU compute, the #1 most requested WSL feature, is now available for preview via the Windows Insider program.</span></span> <span data-ttu-id="d6b2c-106">[Ознакомьтесь с этой записью блога](https://blogs.windows.com/windowsdeveloper/?p=55781).</span><span class="sxs-lookup"><span data-stu-id="d6b2c-106">[Read the blog post](https://blogs.windows.com/windowsdeveloper/?p=55781).</span></span>

## <a name="what-is-gpu-compute"></a><span data-ttu-id="d6b2c-107">Что такое вычисление GPU?</span><span class="sxs-lookup"><span data-stu-id="d6b2c-107">What is GPU compute?</span></span>

<span data-ttu-id="d6b2c-108">Использование ускорения GPU для ресурсоемких задач обычно называется "вычислением GPU".</span><span class="sxs-lookup"><span data-stu-id="d6b2c-108">Leveraging GPU acceleration for compute-intensive tasks is generally referred  to as "GPU compute".</span></span> <span data-ttu-id="d6b2c-109">В вычислениях GPU используется графический процессор (графический процессор) для ускорения математических рабочих нагрузок и параллельная обработка для выполнения требуемых вычислений быстрее, во многих случаях, чем с использованием только ЦП.</span><span class="sxs-lookup"><span data-stu-id="d6b2c-109">GPU computing leverages the GPU (graphics processing unit) to accelerate math heavy workloads and uses its parallel processing to complete the required calculations faster, in many cases, than utilizing only a CPU.</span></span> <span data-ttu-id="d6b2c-110">Такая параллелизации позволяет значительно повысить скорость обработки для этих математических рабочих нагрузок при запуске на ЦП.</span><span class="sxs-lookup"><span data-stu-id="d6b2c-110">This parallelization enables significant processing speed improvements for these math heavy workloads then when running on a CPU.</span></span> <span data-ttu-id="d6b2c-111">Обучающие модели машинного обучения — это отличный пример, в котором вычисления GPU могут значительно ускорить время выполнения этой ресурсоемких задач.</span><span class="sxs-lookup"><span data-stu-id="d6b2c-111">Training machine learning models is a great example in which GPU compute can significantly accelerate the time to complete this computationally expensive task.</span></span>

## <a name="install-and-set-up"></a><span data-ttu-id="d6b2c-112">Установка и настройка</span><span class="sxs-lookup"><span data-stu-id="d6b2c-112">Install and set up</span></span>

<span data-ttu-id="d6b2c-113">Узнайте больше о поддержке WSL 2 и о том, как начать обучение моделей машинного обучения в рамках [руководства по ускоренному использованию GPU](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) в документах директмл. В этом руководстве рассматриваются следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="d6b2c-113">Learn more about WSL 2 support and how to start training machine learning models in the [GPU Accelerated Training guide](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) inside the DirectML docs. This guide covers:</span></span>

* <span data-ttu-id="d6b2c-114">Руководство для начинающих пользователей или учащихся по настройке TensorFlow с помощью Директмл</span><span class="sxs-lookup"><span data-stu-id="d6b2c-114">Guidance for beginners or students to set up TensorFlow with DirectML</span></span>
* <span data-ttu-id="d6b2c-115">Рекомендации для специалистов по началу работы с собственными рабочими процессами CUDA ML</span><span class="sxs-lookup"><span data-stu-id="d6b2c-115">Guidance for professionals to start running their exisiting CUDA ML workflows</span></span>
