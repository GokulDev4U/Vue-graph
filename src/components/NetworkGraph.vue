<template>
  <div class="w-full h-screen bg-gray-800">
    <v-network-graph :nodes="nodes" :edges="edges" :configs="configs" :layouts="layouts"
      style="width: 100%; height: 100vh;" />
  </div>
</template>

<script>
import { defineComponent, reactive } from 'vue';
import { VNetworkGraph, defineConfigs } from 'v-network-graph';
import 'v-network-graph/lib/style.css';

export default defineComponent({
  components: { VNetworkGraph },
  setup() {
    const initialConfigs = defineConfigs({
      node: {
        size: 30,
        label: {
          fontSize: 11,
        },
      },
      edge: {
        width: 1.5,
      },
    });
    const configs = reactive(initialConfigs);

    const nodes = reactive({
      0: { name: "0. Foundations" },
      1: { name: "1. Basic ROS2" },
      2: { name: "2. ROS Basics" },
      3: { name: "3. Intermediate ROS2" },
      4: { name: "4. Robotics Theory" },
      5: { name: "5. Navigation ROS2" },
      6: { name: "C++ Basics for robotics" },
      7: { name: "7. Manipulation" },
      8: { name: "8. Robot Creation" },
      9: { name: "9. Artificial Intelligence" },
      10: { name: "10. ROS Debugging" },
      11: { name: "11. Course of product" },
      12: { name: "12. Web Devel for Robots" },
      13: { name: "13. Simulation" },
      14: { name: "14. Enterprise" },
      15: { name: "Advanced Modern C++ for robotics" },
      16: { name: "Linux for robotics" },
      17: { name: "Behavior Trees for ROS2" },
      18: { name: "ROS2 Control" },
      19: { name: "ROS2 Basics in 5 days (C++)" },
      20: { name: "ROS2 Basics in 5 days (Python)" },
      21: { name: "ROS2 Security" },
      22: { name: "ROS2 Basics in 3 days (Rust)" },
      23: { name: "RTAB" },
      24: { name: "Nav2 Basics" },
      25: { name: "Nav Advanced" },
      26: { name: "TF in ROS2" },
      27: { name: "URDF robot modelling ROS2" },
      28: { name: "ROS1-ROS2 Migration" },
      29: { name: "Python 3 for robotics" },
      30: { name: "Gazebo Sim with ROS2" },
      31: { name: "create a link" },
      32: { name: "Intermediate ROS2 (Python)" },
      33: { name: "Intermediate ROS2 (C++)" },
    });

    const edges = reactive([
      { source: 0, target: 1 },
      { source: 1, target: 3 },
      { source: 1, target: 5 },
      { source: 1, target: 27 },
      { source: 1, target: 28 },
      { source: 3, target: 19 },
      { source: 3, target: 20 },
      { source: 3, target: 32 },
      { source: 3, target: 33 },
      { source: 3, target: 17 },
      { source: 3, target: 18 },
      { source: 5, target: 22 },
      { source: 5, target: 23 },
      { source: 5, target: 24 },
      { source: 5, target: 25 },
      { source: 2, target: 6 },
      { source: 2, target: 13 },
      { source: 0, target: 16 },
      { source: 1, target: 26 },
      { source: 1, target: 29 },
      { source: 2, target: 30 },
      { source: 0, target: 31 },
      // { source: 4, target: 3 },
      { source: 8, target: 30 },
      // { source: 12, target: 10 },
    ]);

    const layouts = reactive({
      nodes: {
        0: { x: 500, y: 700 },
        1: { x: 500, y: 550 },
        2: { x: 350, y: 600 },
        3: { x: 650, y: 400 },
        4: { x: 500, y: 250 },
        5: { x: 800, y: 500 },
        6: { x: 350, y: 450 },
        7: { x: 850, y: 600 },
        8: { x: 200, y: 700 },
        9: { x: 650, y: 200 },
        10: { x: 900, y: 200 },
        11: { x: 250, y: 500 },
        12: { x: 900, y: 400 },
        13: { x: 300, y: 300 },
        14: { x: 450, y: 300 },
        15: { x: 150, y: 650 },
        16: { x: 350, y: 750 },
        17: { x: 600, y: 500 },
        18: { x: 400, y: 400 },
        19: { x: 500, y: 400 },
        20: { x: 700, y: 450 },
        21: { x: 750, y: 550 },
        22: { x: 900, y: 550 },
        23: { x: 750, y: 600 },
        24: { x: 850, y: 500 },
        25: { x: 900, y: 450 },
        26: { x: 750, y: 350 },
        27: { x: 600, y: 250 },
        28: { x: 550, y: 150 },
        29: { x: 650, y: 300 },
        30: { x: 450, y: 500 },
        31: { x: 500, y: 600 },
        32: { x: 600, y: 600 },
        33: { x: 650, y: 500 },
      },
    });

    return { nodes, edges, configs, layouts };
  },
});
</script>

<style>
html,
body {
  height: 100%;
  margin: 0;
}
</style>

