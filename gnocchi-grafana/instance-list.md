## step 1: 
```
curl -i -X POST http://192.168.147.130:35357/v3/auth/tokens -H "Content-type: application/json" -d '{"auth": {"identity": {"methods": ["password"], "password": {"user" : {"id": "09fd1ed8be4b4805be52afd1d06ec044", "password": "admin"}}}, "scope" : {"project" : {"id" : "0c05d69ecac3431d9853657b30e5de6d"}}}}' | grep Token
```

## step 2:
```
curl -g -i -X 'GET' 'http://192.168.147.130:8041/v1/resource/instance' -H 'X-Auth-Token: 6a87be2d125a4be89f8b89f859408f11'
```

## instance info:
```
[
    {
        "created_by_user_id": "3d69cde6ad9845ebb3c1fca855f6b5a8",
        "started_at": "2017-04-10T06:33:48.269454+00:00",
        "revision_start": "2017-04-10T07:00:56.017014+00:00",
        "revision_end": null,
        "ended_at": null,
        "creator": "3d69cde6ad9845ebb3c1fca855f6b5a8:e2445b2e30a84121b507db79fe717577",
        "created_by_project_id": "e2445b2e30a84121b507db79fe717577",
        "metrics": {
            "cpu_l3_cache": "c1600e99-6c2c-44c9-b04f-389525e026e8",
            "disk.write.requests.rate": "162f5163-85f7-483f-962d-707dfb5d0112",
            "perf.cache.misses": "b1b1917e-1ba2-4c14-9901-1b7569f76d8e",
            "perf.cache.references": "e93262d5-f982-4a00-9682-f3ce5e54d0aa",
            "disk.latency": "ac42ff7c-d20d-4e93-a78d-71d9028ee72c",
            "disk.ephemeral.size": "ecf687fb-a943-4d5a-b2b1-6f9ca47e0d51",
            "disk.read.requests": "00e3973a-f6e3-45d4-8c9a-ef8847632b53",
            "perf.cpu.cycles": "360e4db5-3554-4e22-b326-e83d10559712",
            "disk.write.bytes": "740fe1d1-e654-4ecc-84cf-e0ba15f8bd02",
            "disk.capacity": "304b446e-ead2-4b66-883f-0713d3ac3588",
            "vcpus": "8054460d-c67f-47f9-9702-deac9d3d04fb",
            "disk.usage": "ed596873-7e60-4f5c-a2b6-1f3b712720c8",
            "disk.read.bytes.rate": "0da34e01-eb73-45ce-9ae1-0bcacdf9a310",
            "cpu_util": "3c8bb36b-ed18-4b43-a48e-49f0ed69dab0",
            "memory.bandwidth.total": "c0e8bc57-80de-4c18-80b8-5e0c143d4853",
            "memory": "8ba81a6a-08a0-46a1-ab75-c5a28d70cd4b",
            "disk.write.bytes.rate": "d50fcb27-aba9-4d14-8f06-e087630f1c67",
            "memory.usage": "cd853af7-786d-42d1-a633-8ece7aa81b18",
            "cpu.delta": "6eb0be23-f9aa-4c5c-abed-4980b7bebee3",
            "compute.instance.booting.time": "1f802e30-0ea7-4e2f-abc4-fb6a2c79b261",
            "perf.instructions": "d7fd0c8d-ee73-43d3-a942-a79b53ca6d7a",
            "disk.read.requests.rate": "9278830e-ccc3-40f7-9749-d4ad20af1560",
            "disk.iops": "2579a364-5b16-4412-bca7-ea869d64b939",
            "memory.bandwidth.local": "7a5f1a52-fce0-48b6-89e6-ca0e21e56f20",
            "disk.allocation": "becccb25-ec82-40e5-ab9a-e85f0ef2275c",
            "disk.write.requests": "c760268e-d659-41b7-a4d5-5eea3507a1de",
            "disk.root.size": "c0275657-b287-43c3-af40-91a287a887be",
            "memory.resident": "0a834902-609e-4add-9e76-5aeeb0158ac5",
            "disk.read.bytes": "9eb96a1f-2895-4b54-a865-cfdad37300ea",
            "cpu": "1b5f7d45-536a-4db8-8cc2-8a80a224896e"
        },
        "host": "compute.control01",
        "image_ref": "526b734d-2cbd-47ae-b8e1-8c280baa0c68",
        "flavor_id": "1",
        "server_group": null,
        "original_resource_id": "a67170a3-a81b-4bd2-a6b7-2c7136195ffd",
        "user_id": "09fd1ed8be4b4805be52afd1d06ec044",
        "project_id": "0c05d69ecac3431d9853657b30e5de6d",
        "type": "instance",
        "id": "a67170a3-a81b-4bd2-a6b7-2c7136195ffd",
        "display_name": "test1"
    },
    {
        "created_by_user_id": "3d69cde6ad9845ebb3c1fca855f6b5a8",
        "started_at": "2017-04-10T06:36:10.424675+00:00",
        "revision_start": "2017-04-10T07:00:56.049747+00:00",
        "revision_end": null,
        "ended_at": null,
        "creator": "3d69cde6ad9845ebb3c1fca855f6b5a8:e2445b2e30a84121b507db79fe717577",
        "created_by_project_id": "e2445b2e30a84121b507db79fe717577",
        "metrics": {
            "cpu_l3_cache": "3d736821-127e-479f-83a4-50297335a4bd",
            "disk.write.requests.rate": "62c2e95a-32fe-4534-9243-0956cd23ca40",
            "perf.cache.misses": "4427defe-81fd-4891-99a4-df81fa8b0943",
            "perf.cache.references": "aa3095df-0e01-4bbf-bdb7-a9912749a144",
            "disk.latency": "58fd4fd8-b2bf-4924-b098-34b9683378ce",
            "disk.ephemeral.size": "a6417d6c-bca4-4656-9c73-b111a31dab96",
            "disk.read.requests": "5dcdca84-68f1-45f3-ab61-88274e941ae8",
            "perf.cpu.cycles": "b009e38b-ccc0-4d6f-9abb-d04970702f37",
            "disk.write.bytes": "6ebb29dd-0507-47de-a1e0-84e964c8f656",
            "disk.capacity": "6c513c8e-968a-471a-81fa-19f9b39e7133",
            "vcpus": "656b8689-14a4-44e3-8927-d877ba09887b",
            "disk.usage": "5e6d5157-80bd-444a-b055-413652436811",
            "disk.read.bytes.rate": "d7e09f95-61a8-46a2-9db5-92ed5c383d4d",
            "cpu_util": "9dc805a9-049b-43f2-846e-a6a033b81105",
            "memory.bandwidth.total": "e677a06d-3282-4703-a323-7ae8db2dea1f",
            "memory": "0b588f89-1ecd-4100-a740-fc6887faff2d",
            "disk.write.bytes.rate": "bb468dc9-8951-47b2-a19a-f5e1629e6fef",
            "memory.usage": "6f960245-01f8-47d1-8b63-2969be0030d2",
            "cpu.delta": "b6fd9e21-8217-4b56-aa42-8044d4d3265e",
            "compute.instance.booting.time": "fbebdfb1-f393-4eb5-aa93-924075671e1a",
            "perf.instructions": "1820e379-82c6-4550-b784-939caaa7ce2b",
            "disk.read.requests.rate": "e35092b7-603e-4093-9664-60addcd68739",
            "disk.iops": "41f2b16c-532d-4316-935f-dc8fbb2fde2f",
            "memory.bandwidth.local": "01ba7b09-6797-4c83-a942-c2eed0b727b1",
            "disk.allocation": "1a621d98-453a-435e-ac4e-a3e1f1cac245",
            "disk.write.requests": "8ad20d5b-d431-4b2f-9223-e5bfdfc42634",
            "disk.root.size": "59da34f9-1826-4b51-a4bd-b071d4df5d4b",
            "memory.resident": "5aa57e9a-dfd6-4fd2-a441-a238b30d7f2a",
            "disk.read.bytes": "4787aaa2-a918-40b7-ab3f-6cfd8461f403",
            "cpu": "4b3f9433-78e0-48fe-bf1c-d3b6bbe017de"
        },
        "host": "compute.control01",
        "image_ref": "526b734d-2cbd-47ae-b8e1-8c280baa0c68",
        "flavor_id": "1",
        "server_group": null,
        "original_resource_id": "b3e3b2f8-0def-470d-b11e-4cc2bcce9202",
        "user_id": "09fd1ed8be4b4805be52afd1d06ec044",
        "project_id": "0c05d69ecac3431d9853657b30e5de6d",
        "type": "instance",
        "id": "b3e3b2f8-0def-470d-b11e-4cc2bcce9202",
        "display_name": "test2"
    }
]
```
